

```markdown
Register 20.101. LP_SYSTEM_LP_CORE_AHB_TIMEOUT_REG (0x01B0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | LP_SYSTEM_LP2HP_AHB_TIMEOUT_THRES | LP_SYSTEM_LP_CORE_AHB_TIMEOUT_THRES | LP_SYSTEM_LP2HP_AHB_TIMEOUT_EN | LP_SYSTEM_LP_CORE_AHB_TIMEOUT_EN | Reset |
| Value | 0x1f |    |    |    |    |    |    |    |            |                 |                          |                     |                    | Oxffff |       | 1     |

LP_SYSTEM_LP_CORE_AHB_TIMEOUT_EN Configures whether or not to enable timeout protection on LP AHB bus.
- 0: Disable
- 1: Enable
(R/W)

LP_SYSTEM_LP_CORE_AHB_TIMEOUT_THRES Configures LP_CORE_AHB_TIMEOUT_INT threshold. (R/W)

LP_SYSTEM_LP2HP_AHB_TIMEOUT_EN Configures whether or not to enable timeout protection on LP2HP AHB bus.
- 0: Disable
- 1: Enable
(R/W)

LP_SYSTEM_LP2HP_AHB_TIMEOUT_THRES Configures LP_CORE_AHB_TIMEOUT_INT threshold. (R/W)
```