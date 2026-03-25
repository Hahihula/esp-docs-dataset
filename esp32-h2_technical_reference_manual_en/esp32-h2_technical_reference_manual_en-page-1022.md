

```markdown
Register 34.18. TWAI_CLOCK_DIVIDER_REG (0x007C)

TWAI_CD Configures the divisor of the external CLKOUT pin. (R/W)

TWAI_CLOCK_OFF Configures whether or not to enable the external CLKOUT pin in Reset mode.
O: Enable the external CLKOUT pin
1: Disable the external CLKOUT pin
(RO | R/W)
```

```markdown
Register 34.19. TWAI_SW_STANDBY_CFG_REG (0x0080)

TWAI_SW_STANDBY_CLR Configures whether to clear standby signals with software.
O: No effect
1: Clear standby signals
(R/W | R/W)

TWAI_SW_STANDBY_EN Configures whether to set standby signals with software.
O: No effect
1: Set standby signals
(R/W | R/W)
```