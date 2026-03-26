

```markdown
Register 20.89. LP_SYSTEM_LP_CLK_CTRL_REG (0x000C)

LP_SYSTEM_CLK_EN Configures whether the register clock is always on.
O: The clock is enabled only during register access
1: The clock is always on
(R/W)
```

```markdown
Register 20.90. LP_SYSTEM_LP_RST_CTRL_REG (0x0010)

LP_SYSTEM_ANA_RST_BYPASS Configures whether or not to bypass this analog reset sources:
brown-out detector, super WDT and power glitch detector.
O: Not bypass
1: Bypass
(R/W)

LP_SYSTEM_SYS_RST_BYPASS Configures whether or not to bypass this digital reset sources: software, HP watchdog timer, LP watchdog time and eFuse.
O: Not bypass
1: Bypass
(R/W)
```