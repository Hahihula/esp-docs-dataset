

```markdown
## Register 9.11. PCR_TWAI1_CONF_REG (0x0030)

PCR_TWAI1_CLK_EN Configures whether or not to enable TWAI1 APB_CLK.
- O: Not enable
- 1: Enable
(R/W)

PCR_TWAI1_RST_EN Configures whether or not to reset TWAI1.
- O: Not reset
- 1: Reset
(R/W)

PCR_TWAI1_READY Represents whether or not TWAI1 is released from reset.
- O: Not released
- 1: Released
(RO)
```

```markdown
## Register 9.12. PCR_TWAI1_FUNC_CLK_CONF_REG (0x0034)

PCR_TWAI1_FUNC_CLK_SEL Configures the clock source of TWAI1.
- O (default): XTAL_CLK
- 1: RC_FAST_CLK
(R/W)

PCR_TWAI1_FUNC_CLK_EN Configures whether or not to enable TWAI1 functional clock.
- O: Not enable
- 1: Enable
(R/W)
```