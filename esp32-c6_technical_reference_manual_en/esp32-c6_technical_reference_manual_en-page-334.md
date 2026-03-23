

```markdown
## Register 8.24. PCR_TWAI1_CONF_REG (0x0064)

PCR_TWAI1_CLK_EN Configures whether or not to enable TWAI1 APB clock.
- O: Not enable
- 1: Enable
(R/W)

PCR_TWAI1_RST_EN Configures whether or not to reset TWAI1 module.
- O: Not reset
- 1: Reset
(R/W)
```

```markdown
## Register 8.25. PCR_TWAI1_FUNC_CLK_CONF_REG (0x0068)

PCR_TWAI1_FUNC_CLK_SEL Configures to select clock source.
- O (default): Select XTAL_CLK
- 1: Select RC_FAST_CLK
(R/W)

PCR_TWAI1_FUNC_CLK_EN Configures whether or not to enable TWAI1 function clock.
- O: Not enable
- 1: Enable
(R/W)
```