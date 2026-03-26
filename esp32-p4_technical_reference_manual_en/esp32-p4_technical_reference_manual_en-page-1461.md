

```markdown
Register 26.5. ECC_MULT_CONF_REG (0x001C)

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

ECC_MULT_MEM_CLOCK_GATE_FORCE_ON Configures whether to force on ECC memory clock gate.
O: No effect
1: Force on
(R/W)
```

Register 26.6. ECC_MULT_DATE_REG (0x00FC)

```markdown
31                                 28                 27                         0
+-------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 |                                                                                               |
|   |   |   |   |                                                                                               |
|   |   |   |   |                                                                                               |
|   |   |   |   |                                                                                               |
|   |   |   |   |                                                                                               |
+-------------------------------------------------------------------------------------------------+
| 0x2408120                                                                                         |
| Reset                                                                                             |

(reserved) ECC_MULT_DATE

ECC_MULT_DATE Version control register. (R/W)
```