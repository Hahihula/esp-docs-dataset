

```markdown
Chapter 23 ECC Accelerator (ECC)

GoBack

23.4.2.8 Mod Addition (Mod Add)
R = A + B mod N

Mod Addition can be represented as:

where,
* Input:
    - A and B are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py`.
    - The value of N is related to the register fields below:
        * `ECC_MULT_CURVE_MODE` to select the related curve.
        * `ECC_MULT_MOD_BASE` to choose using mod base or order of the base point.
* Output: R is stored in `ECC_MULT_Mem_Px`.

23.4.2.9 Mod Subtraction (Mod Sub)
R = A - B mod N

Mod Subtraction can be represented as:

where,
* Input:
    - A and B are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py`.
    - The value of N is related to the register fields below:
        * `ECC_MULT_CURVE_MODE` to select the related curve.
        * `ECC_MULT_MOD_BASE` to choose using mod base or order of the base point.
* Output: R is stored in `ECC_MULT_Mem_Px`.

23.4.2.10 Mod Multiplication (Mod Multi)
R = A · B mod N

Mod Multiplication can be represented as:

where,
* Input:
    - A and B are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py`.
    - The value of N is related to the register fields below:
        * `ECC_MULT_CURVE_MODE` to select the related curve.
        * `ECC_MULT_MOD_BASE` to choose using mod base or order of the base point.
* Output: R is stored in `ECC_MULT_Mem_Py`.
```