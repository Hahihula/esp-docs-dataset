

```markdown
Chapter 26 ECC Accelerator (ECC)

GoBack

26.4.2.8 Mod Addition (Mod Add)

Mod Addition can be represented as:

R = A + B mod N

where,

• Input:
    – A and B are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py`.
    – The value of N is related to the register fields below:
        * `ECC_MULT_CURVE_MODE` to select the related curve.
        * `ECC_MULT_MOD_BASE` to choose using mod base or order of the base point.

• Output: R is stored in `ECC_MULT_Mem_Px`.

26.4.2.9 Mod Subtraction (Mod Sub)

Mod Subtraction can be represented as:

R = A - B mod N

where,

• Input:
    – A and B are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py`.
    – The value of N is related to the register fields below:
        * `ECC_MULT_CURVE_MODE` to select the related curve.
        * `ECC_MULT_MOD_BASE` to choose using mod base or order of the base point.

• Output: R is stored in `ECC_MULT_Mem_Px`.

26.4.2.10 Mod Multiplication (Mod Multi)

Mod Multiplication can be represented as:

R = A · B mod N

where,

• Input:
    – A and B are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py`.
    – The value of N is related to the register fields below:
        * `ECC_MULT_CURVE_MODE` to select the related curve.
        * `ECC_MULT_MOD_BASE` to choose using mod base or order of the base point.

• Output: R is stored in `ECC_MULT_Mem_Py`.
```