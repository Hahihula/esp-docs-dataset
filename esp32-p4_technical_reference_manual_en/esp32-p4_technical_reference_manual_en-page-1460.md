

```markdown
Register 26.5. ECC_MULT_CONF_REG (0x001C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 |                                                                             |
| 30  |                                 |                                                                             |
| 29  |                                 |                                                                             |
| 28  |                                 |                                                                             |
|     | ECC_MULT_START                 | Configures whether to start the calculation of the ECC accelerator. This bit will be self-cleared when the calculation is done.<br>0: No effect<br>1: Start the calculation of the ECC accelerator (R/W/SC) |
|     | ECC_MULT_RESET                 | Configures whether to reset the ECC accelerator.<br>0: No effect<br>1: Reset (WT) |
|     | ECC_MULT_CURVE_MODE            | Configures the curve mode of the ECC accelerator.<br>0: P-192<br>1: P-256<br>2: P-384<br>3: Invalid (R/W) |
|     | ECC_MULT_MOD_BASE              | Configures whether to choose using the mod base or order of base point in the mod operation. Only valid in working modes 8-11.<br>0: n (order of base point)<br>1: p (mod base of curve) (R/W) |
|     | ECC_MULT_WORK_MODE             | Configures the working mode of the ECC accelerator.<br>0: Affine Point Multi mode<br>1: Reserved<br>2: Affine Point Verif mode<br>3: Affine Point Verif + Multi mode<br>4: Jacobian Point Multi mode<br>5: Point Add mode<br>6: Jacobian Point Verif mode<br>7: Affine Point Verif + Jacobian Point Multi mode<br>8: Mod Add mode<br>9: Mod Sub mode<br>10: Mod Multi mode<br>11: Mod Div mode |
```