

```markdown
Register 10.70. LP_CLKRST_HP_SDMMC_EMAC_RST_CTRL_REG (0x004C)

LP_CLKRST_RST_EN_SDMMC Configures whether to reset SDMMC.
O: Release from reset
1: Reset
(R/W)

LP_CLKRST_FORCE_NORST_SDMMC Configures whether SDMMC can be reset.
O: Can be reset
1: Force not to be reset
(R/W)

LP_CLKRST_RST_EN_EMAC Configures whether to reset EMAC.
O: Release from reset
1: Reset
(R/W)

LP_CLKRST_FORCE_NORST_EMAC Configures whether EMAC can be reset.
O: Can be reset
1: Force not to be reset
(R/W)
```

```markdown
Register 10.71. LP_CLKRST_DATE_REG (0x03FC)

LP_CLKRST_CLK_EN Configures resister clock gating.
O: Support clock only when application writes registers
1: Force on clock gating for registers
(R/W)
```