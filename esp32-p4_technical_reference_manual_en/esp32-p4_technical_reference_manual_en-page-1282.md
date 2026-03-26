

```markdown
Register 20.45. HP_SYSTEM_HP_CORE_AHB_TIMEOUT_REG (0x0120)

31                                 17                                 16                                 1                                    0
+-------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Oxffff | Reset |
+-------------------------------------------------------------------------------------------------+

HP_SYSTEM_CORE_AHB_TIMEOUT_EN Configures whether or not to enable timeout protection on
HP CPUO/1 AHB bus. (R/W)

HP_SYSTEM_CORE_AHB_TIMEOUT_THRES Configures HP CPUO/1 AHB bus timeout threshold.
(R/W)


Register 20.46. HP_SYSTEM_HP_CORE_IBUS_TIMEOUT_REG (0x0124)

31                                 17                                 16                                 1                                    0
+-------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Oxffff | Reset |
+-------------------------------------------------------------------------------------------------+

HP_SYSTEM_CORE_IBUS_TIMEOUT_EN Configures whether or not to enable timeout protection on
HP CPUO/1 IBUS. (R/W)

HP_SYSTEM_CORE_IBUS_TIMEOUT_THRES Configures HP CPUO/1 IBUS timeout threshold. (R/W)
```