
```markdown
| ECC_MULT_KEY_LENGTH | Elliptic Curves* |
|----------------------|------------------|
| 0                    | FIPS P-192       |
| 1                    | FIPS P-256       |

\* See definition of FIPS P-192 and P-256 in [FIPS 186-5](#).

## 20.4.2 Working Modes

ESP32-C61’s ECC accelerator supports 11 working modes based on two elliptic curves described in the above section. By configuring the `ECC_MULT_WORK_MODE` field, users can select the desired working mode. For details, see Table 20.4-2.

Table 20.4-2. Working Modes of ECC Accelerator

| ECC_MULT_WORK_MODE | Working Modes                     |
|--------------------|-----------------------------------|
| 0                  | Affine Point Multi                |
| 1                  | Reserved                          |
| 2                  | Affine Point Verif                |
| 3                  | Affine Point Verif + Multi        |
| 4                  | Jacobian Point Multi              |
| 5                  | Point Add                         |
| 6                  | Jacobian Point Verif              |
| 7                  | Affine Point Verif + Jacobian Point Multi |
| 8                  | Mod Add                           |
| 9                  | Mod Sub                           |
| 10                 | Mod Multi                         |
| 11                 | Mod Div                           |

**Note:**
> Note that the calculation of Jacobian Point Multi mode is about 10% faster than that of the Affine Point Multi mode.

Detailed descriptions about different working modes are provided in the following sections.

### 20.4.2.1 Affine Point Multiplication (Affine Point Multi)

Affine Point Multiplication can be represented as:

$$Q = (Q_x, Q_y) = (J_x, J_y, J_z) = k \cdot (P_x, P_y)$$

where,

*   $(Q_x, Q_y)$ is the affine expression of point $Q$.
*   $(J_x, J_y, J_z)$ is the Jacobian expression of point $Q$.
*   Input: $P_x$, $P_y$, and $k$ are stored in `ECC_MULT_Mem_Px`, `ECC_MULT_Mem_Py`, and `ECC_MULT_Mem_k` respectively.
```