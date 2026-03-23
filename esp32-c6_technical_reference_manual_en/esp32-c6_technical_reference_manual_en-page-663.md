

```markdown
Register 20.5. ECC_MULT_CONF_REG (0x001C)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | ECC_MULT_MEM_CLOCK_GATE_FORCE_ON    |                                                                             |
| 30  | (reserved)                          |                                                                             |
| 9   | ECC_MULT_VERIFICATION_RESULT        | Represents the verification result of ECC Accelerator, valid only when calculation is done. (R/SS) |
| 8   | ECC_MULT_WORK_MODE                  | Configures the work mode of ECC Accelerator.<br>0: Point Multi mode<br>1: Reserved<br>2: Point Verif mode<br>3: Point Verif + Multi mode<br>4: Jacobian Point Multi mode<br>5: Reserved<br>6: Jacobian Point Verif mode<br>7: Point Verif + Jacobian Point Multi mode (R/W) |
| 7   | ECC_MULT_SECURITY_MODE              | Reserved. (R/W)                                                             |
| 6   | ECC_MULT_KEY_LENGTH                 | Configures the key length mode bit of ECC Accelerator.<br>0: P-192<br>1: P-256 (R/W) |
| 5   | ECC_MULT_CLK_EN                     | Configures whether to force on register clock gate.<br>0: No effect<br>1: Force on (R/W) |
| 4   | ECC_MULT_START                      | Configures whether to start calculation of ECC Accelerator. This bit will be self-cleared after the calculation is done.<br>0: No effect<br>1: Start calculation of ECC Accelerator (R/W/SC) |
| 3   | ECC_MULT_RESET                      | Configures whether to reset ECC Accelerator.<br>0: No effect<br>1: Reset (WT) |

Continued on the next page...
```