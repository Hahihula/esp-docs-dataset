

```markdown
- (Rx, Ry) is the affine expression of point R.
- (Jx, Jy, Jz) is the Jacobian expression of point R.
- 1 in the point's Jacobian coordinates is automatically completed by hardware.

• Input:
    - Px and Py are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py.
    - Qx, Qy, and Qz are stored in ECC_MULT_Mem_Qx, ECC_MULT_Mem_Qy, and ECC_MULT_Mem_Qz.

• Output:
    - Rx and Ry are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py.
    - Jx, Jy and Jz are stored in ECC_MULT_Mem_Qx, ECC_MULT_Mem_Qy, and ECC_MULT_Mem_Qz.


### 20.4.2.6 Jacobian Point Verification (Jacobian Point Verif)

Jacobian Point Verification can be used to verify if point (Qx, Qy, Qz) is on a selected elliptic curve.

• (Qx, Qy, Qz) is the Jacobian expression of point Q.
• Input: Qx, Qy, and Qz are stored in ECC_MULT_Mem_Qx, ECC_MULT_Mem_Qy, and ECC_MULT_Mem_Qz respectively.
• Output: The verification result is stored in the ECC_MULT_VERIFICATION_RESULT bit.


### 20.4.2.7 Affine Point Verification + Jacobian Point Multiplication (Affine Point Verif + Jacobian Point Multi)

In this mode, ECC first verifies if point (Px, Py) is on the selected elliptic curve. If so, the following multiplication is performed:

Q = (Qx, Qy, Qz) = k · (Px, Py, 1)

where,

• (Qx, Qy, Qz) is the Jacobian expression of point Q.
• 1 in the point's Jacobian coordinates is automatically completed by hardware.
• Input: Px, Py, and k are stored in ECC_MULT_Mem_Px, ECC_MULT_Mem_Py, and ECC_MULT_Mem_k.
• Output:
    - The verification result is stored in the ECC_MULT_VERIFICATION_RESULT bit.
    - Qx, Qy, and Qz are stored in ECC_MULT_Mem_Qx, ECC_MULT_Mem_Qy, and ECC_MULT_Mem_Qz.


### 20.4.2.8 Mod Addition (Mod Add)

Mod Addition can be represented as:

R = A + B mod N

where,

• Input:
```