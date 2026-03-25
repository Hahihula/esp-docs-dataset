

```markdown
Register 23.5. ECC_MULT_CONF_REG (0x001C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | ECC_MULT_MEM_CLOCK_GATE_FORCE_ON                                           |
| 30  | ECC_MULT_CLK_EN                                                              |
| 29  | ECC_MULT_VERIFICATION_RESULT                                                 |
|     |                                                                             |
| (reserved) |                                                                     |
| 10  | ECC_MULT_SECURITY_MODE                                                      |
| 9   | ECC_MULT_WORK_MODE                                                          |
| 8   | ECC_MULT_MOD_BASE                                                           |
| 7   | ECC_MULT_CURVE_MODE                                                         |
| 6   | ECC_MULT_RESET                                                              |
| 5   | ECC_MULT_START                                                               |

ECC_MULT_START Configures whether to start the calculation of the ECC accelerator. This bit will be self-cleared when the calculation is done.
0: No effect
1: Start the calculation of the ECC accelerator (R/W/SC)

ECC_MULT_RESET Configures whether to reset the ECC accelerator.
0: No effect
1: Reset (WT)

ECC_MULT_CURVE_MODE Configures the curve mode of the ECC accelerator.
0: P-192
1: P-256
2: P-384
3: Invalid (R/W)

ECC_MULT_MOD_BASE Configures whether to choose using the mod base or order of base point in the mod operation. Only valid in working modes 8-11.
0: n (order of base point)
1: p (mod base of curve) (R/W)

Continued on the next page...
```