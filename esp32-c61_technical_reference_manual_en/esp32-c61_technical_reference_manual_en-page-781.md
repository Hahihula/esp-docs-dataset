

```markdown
Register 20.5. ECC_MULT_CONF_REG (0x001C)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            |                                                                             |
| 30  | ECC_MULT_MEM_CLOCK_GATE_FORCE_ON          |                                                                             |
| 29  | ECC_MULT_CLK_EN                           |                                                                             |
| 28  | ECC_MULT_VERIFICATION_RESULT              |                                                                             |
|     | (reserved)                                |                                                                             |
| 9   | ECC_MULT_SECURITY_MODE                    |                                                                             |
| 8   | ECC_MULT_WORK_MODE                        |                                                                             |
| 7   | ECC_MULT_MOD_BASE                         |                                                                             |
| 6   | ECC_MULT_KEY_LENGTH                       |                                                                             |
| 5   | ECC_MULT_RESET                            |                                                                             |
| 4   | ECC_MULT_START                            |                                                                             |
|     |                                            |                                                                             |
| 31  | 30 29 28                                   | 9 8 7 6 5 4 3 2 1 0                                                          |
|-----|--------------------------------------------|-------------------------------------------------------------------------------|
| 0   | 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0           | 0 0 0 0 0 0 0 0 Reset                                                        |

ECC_MULT_START Configures whether to start the calculation of the ECC accelerator. This bit will be self-cleared when the calculation is done.
- O: No effect
- 1: Start the calculation of the ECC accelerator (R/W/SC)

ECC_MULT_RESET Configures whether to reset the ECC accelerator.
- O: No effect
- 1: Reset (WT)

ECC_MULT_KEY_LENGTH Configures the key length of the ECC accelerator.
- 0: P-192
- 1: P-256 (R/W)

ECC_MULT_MOD_BASE Configures whether to choose using the mod base or order of base point in the mod operation. Only valid in working modes 8-11.
- 0: n (order of base point)
- 1: p (mod base of curve) (R/W)

ECC_MULT_WORK_MODE Configures the working mode of the ECC accelerator.
- 0: Affine Point Multi mode
- 1: Reserved
- 2: Affine Point Verif mode
- 3: Affine Point Verif + Multi mode
- 4: Jacobian Point Multi mode
- 5: Point Add mode
- 6: Jacobian Point Verifier mode
- 7: Affine Point Verif + Jacobian Point Multi mode
- 8: Mod Add mode
- 9: Mod Sub mode
- 10: Mod Multi mode
- 11: Mod Div mode (R/W)

Continued on the next page...
```