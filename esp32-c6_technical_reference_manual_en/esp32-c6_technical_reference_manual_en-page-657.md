

```markdown
## 20.4.2 Working Modes

ESP32-C6's ECC accelerator supports six working modes based on two elliptic curves described in the above section. By configuring the `ECC_MULT_WORK_MODE` field, users can choose the desired working mode. For details, see Table 20.4-2.

Table 20.4-2. ECC Accelerator's Working Modes

| ECC_MULT_WORK_MODE | Working Modes          | ECC_MULT_WORK_MODE | Working Modes                  |
|--------------------|------------------------|--------------------|--------------------------------|
| 3'd0               | Point Multi            | 3'd4               | Jacobian Point Multi           |
| 3'd1               | Reserved               | 3'd5               | Reserved                       |
| 3'd2               | Point Verif            | 3'd6               | Jacobian Point Verif           |
| 3'd3               | Point Verif + Multi    | 3'd7               | Point Verif + Jacobian Point Multi |

Detailed descriptions about different working modes are provided in the following sections.

### 20.4.2.1 Base Point Multiplication (Point Multi Mode)

Base Point Multiplication can be represented as:

```
(Qx, Qy) = k · (Px, Py)
```

where,

- Input: `Px`, `Py`, and `k` are stored in `ECC_MULT_Mem_Px`, `ECC_MULT_Mem_Py`, and `ECC_MULT_Mem_k` respectively.
- Output: `Qx` and `Qy` are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py` respectively.

### 20.4.2.2 Base Point Verification (Point Verif Mode)

Base Point Verification can be used to verify if a point `(Px, Py)` is on a selected elliptic curve.

- Input: `Px` and `Py` are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py` respectively.
- Output: the verification result is stored in the `ECC_MULT_VERIFICATION_RESULT` field.

### 20.4.2.3 Base Point Verification + Base Point Multiplication (Point Verif + Multi Mode)

In this working mode, ECC first verifies if Point `(Px, Py)` is on the selected elliptic curve. If so, the following multiplication is performed:

```
(Qx, Qy) = k · (Px, Py)
```

where,

- Input: `Px`, `Py`, and `k` are stored in `ECC_MULT_Mem_Px`, `ECC_MULT_Mem_Py`, and `ECC_MULT_Mem_k` respectively.
- Output:
  - the verification result is stored in the `ECC_MULT_VERIFICATION_RESULT` field.
  - `Qx` and `Qy` are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py` respectively.
```