

```markdown
Register 54.23. SDHOST_ENSHIFT_REG (0x0110)

SDHOST_ENABLE_SHIFT_REG Configures the amount of phase shift provided on the default en-
ables in the design. Two bits are assigned for each card, e.g., bit[1:0] are assigned to card 0.
For every card:
    0x0: Default phase shift
    0x1: Enables shifted to next immediate positive edge
    0x2: Enables shifted to next immediate negative edge
    0x3: Reserved
(R/W)

Register 54.24. SDHOST_CLK_EDGE_SEL_REG (0x0800)

SDHOST_ESDIO_MODE Configures whether to enable eSDIO mode.
    0: Not enable
    1: Enable
(R/W)

SDHOST_ESD_MODE Configures whether to enable eSD mode.
    0: Not enable
    1: Enable
(R/W)
```