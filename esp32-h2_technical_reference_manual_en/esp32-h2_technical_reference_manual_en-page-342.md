

```markdown
Register 7.88. LP_CLKRST_DATE_REG (0x03FC)

LP_CLKRST_CLK_EN Version control register. (R/W)

LP_CLKRST_CLK_EN Configures whether to force enable the clock gate for header registers.
O: Invalid
1: Force enable
(R/W)
```

```markdown
Register 7.89. LP_AON_SYS_CFG_REG (0x0034)

LP_AON_HPSYS_SW_RESET
LP_AON_FORCE_DOWNLOAD_BOOT

(reserved)

| 31 | 30 | 29 |
|----:|----:|----:|
|   O |   O |   O |

Reset
```

```markdown
LP_AON_FORCE_DOWNLOAD_BOOT Configures whether to trigger a CPU reset and switch the chip boot mode.
O: No effect.
1: If EFUSE_DIS_FORCE_DOWNLOAD is 0, software can force switch the chip from SPI Boot mode to Joint Download Boot mode and trigger a CPU reset.
(R/W)

LP_AON_HPSYS_SW_RESET Configures whether to do software reset of the system.
O: Not reset
1: Reset
(WT)
```