

```markdown
- Output: Qx and Qy are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py respectively.
```

## 20.4.2.2 Affine Point Verification (Affine Point Verif)

Affine Point Verification can be used to verify if a point $(P_x, P_y)$ is on a selected elliptic curve.

- Input: Px and Py are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py respectively.
- Output: The verification result is stored in the ECC_MULT_VERIFICATION_RESULT bit.

## 20.4.2.3 Affine Point Verification + Affine Point Multiplication (Affine Point Verif + Multi)

In this mode, ECC first verifies if point $(P_x, P_y)$ is on the selected elliptic curve. If so, the following multiplication is performed:

$$Q = (Q_x, Q_y) = (J_x, J_y, J_z) = k \cdot (P_x, P_y)$$

where,

- $(Q_x, Q_y)$ is the affine expression of point Q.
- $(J_x, J_y, J_z)$ is the Jacobian expression of point Q.
- Input: Px, Py, and k are stored in ECC_MULT_Mem_Px, ECC_MULT_Mem_Py, and ECC_MULT_Mem_k respectively.
- Output:
  - The verification result is stored in the ECC_MULT_VERIFICATION_RESULT bit.
  - $Q_x$ and $Q_y$ are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py respectively.
  - $J_x$, $J_y$, and $J_z$ are stored in ECC_MULT_Mem_Qx, ECC_MULT_Mem_Qy, and ECC_MULT_Mem_Qz.

## 20.4.2.4 Jacobian Point Multiplication (Jacobian Point Multi)

Jacobian Point Multiplication can be represented as:

$$Q = (Q_x, Q_y, Q_z) = k \cdot (P_x, P_y, 1)$$

where,

- $(Q_x, Q_y, Q_z)$ is the Jacobian expression of point Q.
- 1 in the point's Jacobian coordinates is automatically completed by hardware.
- Input: Px, Py, and k are stored in ECC_MULT_Mem_Px, ECC_MULT_Mem_Py, and ECC_MULT_Mem_k respectively.
- Output: $Q_x$, $Q_y$, and $Q_z$ are stored in ECC_MULT_Mem_Qx, ECC_MULT_Mem_Qy, and ECC_MULT_Mem_Qz respectively.

## 20.4.2.5 Point Addition (Point Add)

Point Addition can be represented as:

$$R = (R_x, R_y) = (J_x, J_y, J_z) = (P_x, P_y, 1) + (Q_x, Q_y, Q_z)$$

where,
```