

```markdown
## Register 8.55. PCR_IOMUX_CONF_REG (0x00E8)

PCR_IOMUX_CLK_EN Configures whether or not to enable IO MUX APB clock.
- O: Not enable
- 1: Enable
(R/W)

PCR_IOMUX_RST_EN Configures whether or not to reset IO MUX module.
- O: Not reset
- 1: Reset
(R/W)
```

```markdown
## Register 8.56. PCR_IOMUX_CLK_CONF_REG (0x00EC)

PCR_IOMUX_FUNC_CLK_SEL Configures to select clock source.
- O: Not select any clock
- 1: Select PLL_F8OM_CLK
- 2: Select RC_FAST_CLK
- 3: XTAL_CLK
(R/W)

PCR_IOMUX_FUNC_CLK_EN Configures whether or not to enable IO MUX function clock.
- O: Not enable
- 1: Enable
(R/W)
```