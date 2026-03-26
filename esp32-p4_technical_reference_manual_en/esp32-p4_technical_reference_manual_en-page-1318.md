

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.95. LP_SYSTEM_PAD_COMP1_REG (0x014C)
```

| bit | 31 | 30 | 29 | ... | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|-----|---|---|---|---|---|---|---|---|---|
|     |    |    |    |      |   |   |   | LP_SYSTEM_XPD_COMP1 | LP_SYSTEM_MODE_COMP1 | LP_SYSTEM_DREF_COMP1 | Reset |

LP_SYSTEM_DREF_COMP1 Configures the internal reference voltage of pad comparator1. (R/W)

LP_SYSTEM_MODE_COMP1 Configures the comparison mode for pad comparator1.
0: Comparing the main voltage with the external reference voltage
1: Comparing the main voltage with the internal reference voltage
(R/W)

LP_SYSTEM_XPD_COMP1 Configures whether or not to enable pad comparator1.
0: Disable
1: Enable
(R/W)

Register 20.96. LP_SYSTEM_HP_MEM_AUX_CTRL_REG (0x0180)
```

| bit | 31 | 30 | ... | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|-----|---|---|---|---|---|---|---|---|
|     |    |    |      |   |   |   | LP_SYSTEM_HP_MEM_AUX_CTRL | Reset |

LP_SYSTEM_HP_MEM_AUX_CTRL Configures HP system memory aux control value. (R/W)
```