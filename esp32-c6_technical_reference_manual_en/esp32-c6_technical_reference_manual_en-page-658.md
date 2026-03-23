

```markdown
## 20.4.2.4 Jacobian Point Multiplication (Jacobian Point Multi Mode)

Jacobian Point Multiplication can be represented as:

\[
(Q_x, Q_y, Q_z) = k \cdot (P_x, P_y, 1)
\]

where,

*   $(Q_x, Q_y, Q_z)$ is a Jacobian point on the selected elliptic curve.
*   1 in the point's Jacobian coordinates is auto completed by hardware.
*   Input: $P_x$, $P_y$, and $k$ are stored in `ECC_MULT_Mem_Px`, `ECC_MULT_Mem_Py`, and `ECC_MULT_Mem_k` respectively.
*   Output: $Q_x$, $Q_y$, and $Q_z$ are stored in `ECC_MULT_Mem_Px`, `ECC_MULT_Mem_Py`, and `ECC_MULT_Mem_k` respectively.

## 20.4.2.5 Jacobian Point Verification (Jacobian Point Verif Mode)

Jacobian Point Verification can be used to verify if a point $(Q_x, Q_y, Q_z)$ is on a selected elliptic curve.

*   $(Q_x, Q_y, Q_z)$ is the point in Jacobian Coordinates.
*   Input: $Q_x$, $Q_y$, and $Q_z$ are stored in `ECC_MULT_Mem_Px`, `ECC_MULT_Mem_Py`, and `ECC_MULT_Mem_k` respectively.
*   Output: the verification result is stored in the `ECC_MULT_VERIFICATION_RESULT` field.

## 20.4.2.6 Base Point Verification + Jacobian Point Multiplication (Point Verif + Jacobian Point Multi Mode)

In this working mode, ECC first verifies if Point $(P_x, P_y)$ is on the selected elliptic curve. If so, the following multiplication is performed:

\[
(Q_x, Q_y, Q_z) = k \cdot (P_x, P_y, 1)
\]

where,

*   $(Q_x, Q_y, Q_z)$ is a Jacobian point on the selected elliptic curve.
*   1 in the point's Jacobian coordinates is auto completed by hardware.
*   Input: $P_x$, $P_y$, and $k$ are stored in `ECC_MULT_Mem_Px`, `ECC_MULT_Mem_Py`, and `ECC_MULT_Mem_k`.
*   Output:
    - the verification result is stored in the `ECC_MULT_VERIFICATION_RESULT` field.
    - $Q_x$, $Q_y$, and $Q_z$ are stored in `ECC_MULT_Mem_Px`, `ECC_MULT_Mem_Py`, and `ECC_MULT_Mem_k`.

## 20.5 Clocks and Resets

ESP32-C6's ECC only has one clock module (`CRYPTO_ECC_CLK`) and one reset module (`CRYPTO_ECC_RST`). Users should enable the ECC clock and disable the ECC reset before starting the ECC accelerator. For details on how to configure the ECC clock and reset, please refer to Chapter 8 Reset and Clock.
```