

```markdown
Register 9.83. LP_IOMUX_PADn_REG (n = 0 - 15) (0x0008+4*n)

Continued from the previous page...

LP_IOMUX_PADn_SLP_OE    Configures whether or not to enable the output of GPIO n in sleep mode.
    0: Disable
    1: Enable
    (R/W)

LP_IOMUX_PADn_FUN_IE     Configures whether or not to enable input of GPIO n.
    0: Disable
    1: Enable
    (R/W)

LP_IOMUX_PADn_FILTER_EN   Configures whether or not to enable filter for pin input signals.
    0: Disable
    1: Enable
    (R/W)

Register 9.84. LP_IOMUX_LP_PAD_HOLD_REG (0x004C)
```

```markdown
LP_IOMUX_LP_GPIO_HOLD    Configures whether or not to enable hold function of GPIO n.
    0: Disable
    1: Enable
    (R/W)
```