

```markdown
Register 23.5. ECC_MULT_CONF_REG (0x001C)

Continued from the previous page...

ECC_MULT_WORK_MODE Configures the working mode of the ECC accelerator.
- 0: Affine Point Multi mode
- 1: Reserved
- 2: Affine Point Verif mode
- 3: Affine Point Verif + Multi mode
- 4: Jacobian Point Multi mode
- 5: Point Add mode
- 6: Jacobian Point Verif mode
- 7: Affine Point Verif + Jacobian Point Multi mode
- 8: Mod Add mode
- 9: Mod Sub mode
- 10: Mod Multi mode
- 11: Mod Div mode
(R/W)

ECC_MULT_SECURITY_MODE Configures whether to enhance the anti-attack performance when calculating point multiplication. Only valid in working modes 0, 3, 4, and 7.
- 0: Disable
- 1: Enable
(R/W)

ECC_MULT_VERIFICATION_RESULT Represents the verification result of the ECC accelerator, valid only when the calculation is done.
- 0: Verification failed
- 1: Verification passed
(R/SS)

ECC_MULT_CLK_EN Configures whether to force on register clock gate.
- 0: No effect
- 1: Force on
(R/W)

ECC_MULT_MEM_CLOCK_GATE_FORCE_ON Configures whether to force the ECC memory clock gate on.
- 0: No effect
- 1: Force on
(R/W)
```