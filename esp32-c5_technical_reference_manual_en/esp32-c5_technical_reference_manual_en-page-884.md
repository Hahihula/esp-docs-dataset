

```markdown
- (Jx, Jy, Jz) is the Jacobian expression of point Q.
- Input: Px, Py, and k are stored in ECC_MULT_Mem_Px, ECC_MULT_Mem_Py, and ECC_MULT_Mem_k respectively.
- Output: Qx and Qy are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py respectively.

23.4.2.2 Affine Point Verification (Affine Point Verif)

Affine Point Verification can be used to verify if a point (Px, Py) is on a selected elliptic curve.
- Input: Px and Py are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py respectively.
- Output: The verification result is stored in the ECC_MULT_VERIFICATION_RESULT bit.

23.4.2.3 Affine Point Verification + Affine Point Multiplication (Affine Point Verif + Multi)

In this mode, ECC first verifies if point (Px, Py) is on the selected elliptic curve. If so, the following multiplication is performed:

Q = (Qx, Qy) = (Jx, Jy, Jz) = k · (Px, Py)

where,

- (Qx, Qy) is the affine expression of point Q.
- (Jx, Jy, Jz) is the Jacobian expression of point Q.
- Input: Px, Py, and k are stored in ECC_MULT_Mem_Px, ECC_MULT_Mem_Py, and ECC_MULT_Mem_k respectively.
- Output:
  - The verification result is stored in the ECC_MULT_VERIFICATION_RESULT bit.
  - Qx and Qy are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py respectively.
  - Jx, Jy, and Jz are stored in ECC_MULT_Mem_Qx, ECC_MULT_Mem_Qy, and ECC_MULT_Mem_Qz.

23.4.2.4 Jacobian Point Multiplication (Jacobian Point Multi)

Jacobian Point Multiplication can be represented as:

Q = (Qx, Qy, Qz) = k · (Px, Py, 1)

where,

- (Qx, Qy, Qz) is the Jacobian expression of point Q.
- 1 in the point's Jacobian coordinates is automatically completed by hardware.
- Input: Px, Py, and k are stored in ECC_MULT_Mem_Px, ECC_MULT_Mem_Py, and ECC_MULT_Mem_k respectively.
- Output: Qx, Qy, and Qz are stored in ECC_MULT_Mem_Qx, ECC_MULT_Mem_Qy, and ECC_MULT_Mem_Qz respectively.
```