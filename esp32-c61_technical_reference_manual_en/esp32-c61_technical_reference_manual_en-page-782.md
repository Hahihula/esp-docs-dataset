

```markdown
Register 20.5. ECC_MULT_CONF_REG (0x001C)

Continued from the previous page...

ECC_MULT_SECURITY_MODE Configures whether to enhance the anti-attack performance when calculating point multiplication. Only valid in working modes 0, 3, 4, and 7.
O: Disable
1: Enable
(R/W)

ECC_MULT_VERIFICATION_RESULT Represents the verification result of the ECC accelerator, valid only when the calculation is done.
O: Verification failed
1: Verification passed
(R/SS)

ECC_MULT_CLK_EN Configures whether to force on register clock gate.
O: No effect
1: Force on
(R/W)

ECC_MULT_MEM_CLOCK_GATE_FORCE_ON Configures whether to force the ECC memory clock gate on.
O: No effect
1: Force on
(R/W)
```

```markdown
Register 20.6. ECC_MULT_DATE_REG (0x00FC)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 30  |                     |
| 29  |                     |
| 28  |                     |
| 27  |                     |
|     | ECC_MULT_DATE       |
|     | 0x2401060           |
|     | Reset               |
```

```markdown
ECC_MULT_DATE Version control register. (R/W)
```