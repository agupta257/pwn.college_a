You realise that a previous climber has set up a puzzle in what was otherwise an empty room, blocking the entrance to the next floor on the ceiling. You must slide the blocks forming the pyramid to create a path above.

## What I did
I utilized AI for this challenge, I gave it a prompt and it gave me a python script which is as follows:
```bash
#!/usr/bin/env python3
# solve_sliding_xor.py
# Reconstruct ks and secret from the sliding-XOR cipher used in the challenge.

import binascii
import numpy as np

# ---------------------------
# Challenge inputs (as used)
# ---------------------------
cipher_hex = (
    "b31113bd631c7207ec9587b32e686c8b6df255d66f4a987adacf6c283875ded5d"
    "1633b5f8823fa0b9bbbfab3195f1a51506afd54e03392ae338d872445c9025d88"
    "c8d4425a00a9b4478f86acadbd781df6a4194e376c09145a6f9afcbe02d36b570"
    "9f74d910edf94552dc4680041d6717fea824718c21385bdfd6176f72210054833"
    "6d10ead87f01a95c5497dcb6c2"
)
ct = bytearray(binascii.unhexlify(cipher_hex))

wrapper0 = b'bro i have a cRAzy story to tell you i went to ant4rctica and BOOM i saw a random '
wrapper1 = b' it was crazy like how did it get there??'

# Secret length and L calculation (same formula used by the challenge)
s = 20
w0 = len(wrapper0)
w1 = len(wrapper1)
L = w0 + w1 + 9  # matches challenge code
N = len(ct)

print("N (ciphertext bytes) =", N)
print("w0 =", w0, "w1 =", w1, "s =", s, "L =", L)

# ---------------------------
# Build linear system A x = b over GF(2)
# unknown bits = ks bytes (L) followed by secret bytes (s) -> (L + s) bytes * 8 bits
# rows = N * 8 (bitwise equations)
# ---------------------------
num_unknown_bytes = L + s
rows = N * 8
cols = num_unknown_bytes * 8

A = np.zeros((rows, cols), dtype=np.uint8)
b = np.zeros(rows, dtype=np.uint8)

for p in range(N):
    # indices of ks bytes that are XORed into plaintext position p
    i_min = max(0, p - (L - 1))
    i_max = min(p, N - L)
    ks_indices = [p - i for i in range(i_min, i_max + 1)]
    for bit in range(8):
        row = p * 8 + bit
        # ks bits contribution
        for k in ks_indices:
            A[row, k * 8 + bit] ^= 1
        # contribution from known wrappers or secret variable
        if p < w0:
            # known prefix byte -> move to RHS
            b[row] = ((ct[p] >> bit) & 1) ^ ((wrapper0[p] >> bit) & 1)
        elif p >= w0 + s:
            # known suffix byte -> move to RHS
            idx = p - (w0 + s)
            b[row] = ((ct[p] >> bit) & 1) ^ ((wrapper1[idx] >> bit) & 1)
        else:
            # secret byte unknown -> set variable bit for secret
            secret_idx = p - w0
            A[row, (L + secret_idx) * 8 + bit] ^= 1
            b[row] = (ct[p] >> bit) & 1

print("Built matrix A (rows x cols):", A.shape)

# ---------------------------
# Gaussian elimination over GF(2)
# (simple row-reduction to reduced row-echelon-like form)
# ---------------------------
M = A.copy()
rhs = b.copy()
rowsM, colsM = M.shape
r = 0
pivot_cols = []

for c in range(colsM):
    if r >= rowsM:
        break
    pivot = None
    for i in range(r, rowsM):
        if M[i, c]:
            pivot = i
            break
    if pivot is None:
        continue
    if pivot != r:
        M[[r, pivot]] = M[[pivot, r]]
        rhs[[r, pivot]] = rhs[[pivot, r]]
    # eliminate all other rows that have a 1 in column c
    for i in range(rowsM):
        if i != r and M[i, c]:
            M[i] ^= M[r]
            rhs[i] ^= rhs[r]
    pivot_cols.append(c)
    r += 1

rank = len(pivot_cols)
free_bits = colsM - rank
print("Rank:", rank, "unknown bits:", colsM, "free bits:", free_bits)

# Check consistency
inconsistent = False
for i in range(r, rowsM):
    if rhs[i]:
        inconsistent = True
        break
print("Inconsistent system?:", inconsistent)
if inconsistent:
    raise SystemExit("No solution - inconsistent system")

# Extract particular solution x_part (bits)
x_part = np.zeros(colsM, dtype=np.uint8)
for row_idx in range(rank):
    c = pivot_cols[row_idx]
    x_part[c] = rhs[row_idx]

# Convenience: pack particular solution into bytes
def bits_to_bytes_le(bitarr):
    # bitarr length is multiple of 8, little-endian bit order used in construction
    nbytes = len(bitarr) // 8
    out = bytearray(nbytes)
    for i in range(nbytes):
        byte = 0
        for bit in range(8):
            byte |= (int(bitarr[i*8 + bit]) & 1) << bit
        out[i] = byte
    return bytes(out)

part_bytes = bits_to_bytes_le(x_part)
ks_part = part_bytes[:L]
secret_part = part_bytes[L:L+s]

print("Particular secret bytes (raw):", secret_part)

# Build nullspace basis vectors (each is a bit-vector length colsM)
free_cols = [c for c in range(colsM) if c not in pivot_cols]
nullspace = []
for free_col in free_cols:
    vec = np.zeros(colsM, dtype=np.uint8)
    vec[free_col] = 1
    for row_idx in range(rank):
        c = pivot_cols[row_idx]
        ones = np.nonzero(M[row_idx])[0]
        ssum = 0
        for col in ones:
            if col == c:
                continue
            ssum ^= vec[col]
        vec[c] = ssum
    nullspace.append(vec)

print("Nullspace dimension (bits):", len(nullspace))

# For convenience, build Nmat that maps nullspace coefficients -> secret bit deltas
num_basis = len(nullspace)
Nmat = np.zeros((s * 8, num_basis), dtype=np.uint8)
for j in range(num_basis):
    vec = nullspace[j]
    for i in range(s):
        bits = vec[(L + i) * 8 : (L + i + 1) * 8]
        for bit in range(8):
            Nmat[i*8 + bit, j] = bits[bit]

# ---------------------------
# If you know a format (e.g. starts with 'citadel{' and ends with '}'), impose it:
# ---------------------------
prefix = b'citadel{'  # eight bytes
suffix = b'}'         # final byte must be '}' (optional)
assert len(prefix) <= s
# Build constraints Rows @ alpha = rhs_constr, where alpha are the nullspace bits (coeffs)
rows_cons = []
rhs_cons = []

# prefix constraints
for i, pb in enumerate(prefix):
    for bit in range(8):
        pos = i*8 + bit
        rows_cons.append(Nmat[pos, :].copy())
        current = (secret_part[i] >> bit) & 1
        desired = (pb >> bit) & 1
        rhs_cons.append(current ^ desired)

# suffix constraint (last byte)
if suffix:
    last_idx = s - 1
    for bit in range(8):
        pos = last_idx*8 + bit
        rows_cons.append(Nmat[pos, :].copy())
        current = (secret_part[last_idx] >> bit) & 1
        desired = (suffix[0] >> bit) & 1
        rhs_cons.append(current ^ desired)

RowsC = np.vstack(rows_cons).astype(np.uint8)
rhsC = np.array(rhs_cons, dtype=np.uint8)
print("Constraint rows:", RowsC.shape, "-> solving for nullspace coefficients (alpha)")

# Solve RowsC @ alpha = rhsC over GF(2)
M2 = RowsC.copy()
rhs2 = rhsC.copy()
r2 = 0
piv2 = []
rows2, cols2 = M2.shape
for c in range(cols2):
    if r2 >= rows2: break
    pivot = None
    for i in range(r2, rows2):
        if M2[i, c]:
            pivot = i; break
    if pivot is None: continue
    if pivot != r2:
        M2[[r2, pivot]] = M2[[pivot, r2]]
        rhs2[[r2, pivot]] = rhs2[[pivot, r2]]
    for i in range(rows2):
        if i != r2 and M2[i, c]:
            M2[i] ^= M2[r2]; rhs2[i] ^= rhs2[r2]
    piv2.append(c)
    r2 += 1

# check consistency
for i in range(r2, rows2):
    if rhs2[i]:
        raise SystemExit("No solution matching the enforced prefix/suffix")

# get a particular alpha
alpha_part = np.zeros(cols2, dtype=np.uint8)
for row_idx in range(len(piv2)):
    c = piv2[row_idx]
    alpha_part[c] = rhs2[row_idx]

# compute free alpha nullspace (if any)
free_alpha_cols = [c for c in range(cols2) if c not in piv2]
alpha_null = []
for free_col in free_alpha_cols:
    v = np.zeros(cols2, dtype=np.uint8)
    v[free_col] = 1
    for row_idx in range(len(piv2)):
        c = piv2[row_idx]
        ones = np.nonzero(M2[row_idx])[0]
        ssum = 0
        for col in ones:
            if col == c: continue
            ssum ^= v[col]
        v[c] = ssum
    alpha_null.append(v)

print("Free alpha bits:", len(alpha_null))

# If no free alpha bits, alpha is unique and we can compute the final secret
if len(alpha_null) == 0:
    alpha = alpha_part
else:
    # If there are free bits, one would enumerate or sample combinations.
    # For this challenge we expect small or zero free bits; to be safe, we try a simple sampling:
    found = False
    for mask in range(1 << min(20, len(alpha_null))):
        alpha = alpha_part.copy()
        for i in range(len(alpha_null)):
            if (mask >> i) & 1:
                alpha ^= alpha_null[i]
        # compute secret bytes from alpha
        secret_bits = np.array([ (secret_part[i] >> bit) & 1 for i in range(s) for bit in range(8)], dtype=np.uint8)
        secret_bits ^= (Nmat.dot(alpha) % 2)
        # convert to bytes
        secret_bytes = bytes(
            int("".join(str(int(b)) for b in secret_bits[i*8:(i+1)*8][::-1]), 2)
            for i in range(s)
        )
        try:
            secret_text = secret_bytes.decode('utf-8')
        except:
            continue
        if secret_text.startswith(prefix.decode()) and secret_text.endswith(suffix.decode()):
            print("Found candidate:", secret_text)
            found = True
            break
    if not found:
        raise SystemExit("Didn't find printable secret in sampled alphas")

# If alpha found / unique, compute final secret
# Compute final secret bytes (alpha length == num_basis)
if len(alpha_null) == 0:
    # compute secret bits from alpha_part
    secret_bits = np.array([ (secret_part[i] >> bit) & 1 for i in range(s) for bit in range(8)], dtype=np.uint8)
    secret_bits ^= (Nmat.dot(alpha_part) % 2)
    secret_bytes = bytes(
        int("".join(str(int(b)) for b in secret_bits[i*8:(i+1)*8][::-1]), 2)
        for i in range(s)
    )
else:
    # secret_bytes was set in the sampling enumeration above
    pass

print("Recovered secret:", secret_bytes)

# Reconstruct ks from x_part and alpha (to verify)
# Rebuild full x = x_part XOR sum(alpha_i * nullspace_i)
x_full = x_part.copy()
if len(alpha_null) == 0:
    for j in range(num_basis):
        if alpha_part[j]:
            x_full ^= nullspace[j]
else:
    # if we enumerated a solution, alpha is in variable 'alpha'
    for j in range(num_basis):
        if alpha[j]:
            x_full ^= nullspace[j]

full_bytes = bits_to_bytes_le(x_full)
ks_bytes = full_bytes[:L]
reconstructed_P = bytearray(wrapper0 + secret_bytes + wrapper1)
# re-encrypt
fb = bytearray(reconstructed_P)
for i in range(len(fb) - len(ks_bytes) + 1):
    for j in range(len(ks_bytes)):
        fb[i + j] ^= ks_bytes[j]

if fb == ct:
    print("Verification: re-encryption matches ciphertext. Flag is:", secret_bytes.decode())
else:
    print("Verification failed.")
```

then, I took the hex ciphertext from the challenge and converted it into raw bytes. The script which I used next is
```bash
flag = bytearray(wrapper0 + secret + wrapper1)
for i in range(len(flag) - len(ks) + 1):
    for j in range(len(ks)):
        flag[i + j] ^= ks[j]

wrapper0 = b"bro i have a cRAzy story to tell you i went to ant4rctica and BOOM i saw a random "
wrapper1 = b" it was crazy like how did it get there??"

A · x = b  (mod 2)

prefix = "citadel{"
suffix = "}"
```

The flag I got - citadel{pyr4m1d+x0r}
