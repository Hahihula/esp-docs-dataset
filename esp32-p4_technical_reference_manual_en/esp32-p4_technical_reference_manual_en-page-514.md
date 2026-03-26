

```markdown
Chapter 8 eFuse Controller (EFUSE) GoBack

Register 8.8. EFUSE_RD_REPEAT_DATA4_REG (0x0040)

Continued from the previous page...

EFUSE_HP_PWR_SRC_SEL Represents the HP system power source.
O: LDO
1: DCDC
(RO)

EFUSE_DCDC_VSET_EN Represents whether to use the default voltage configured by EFUSE_DCDC_VSET.
O: Not use
1: Use
(RO)

EFUSE_DIS_WDT Represents whether to disable the watchdog.
O: Enable
1: Disable
(RO)

EFUSE_DIS_SWD Represents whether to disable the super watchdog.
O: Enable
1: Disable
(RO)

Register 8.9. EFUSE_RD_MAC_SYS_O_REG (0x0044)
```
```markdown
31                                 0

EFUSE_MAC_0                      0x0000000 Reset

EFUSE_MAC_0 Represents the low 32 bits of MAC address. (RO)
```