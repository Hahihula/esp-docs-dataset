

```markdown
| 31 | 28 | 27              | 24             | 23                         | (reserved) | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|----:|-----------------|----------------|-----------------------------|------------|---|---|---|---|---|---|---|---|---|
|    |    | Oxf            | Oxf           | PMU_FORCE_HP_MEM_NO_ISO     |            |   |   |   |   |   |   |   |   | Reset |
|    |    |                |               |                             |            |   |   |   |   |   |   |   |   |   |

PMU_FORCE_HP_MEM_ISO Configures whether or not to enable the force isolation of Internal SRAMx domain.
O: No effect
1: Enable
(R/W)

PMU_FORCE_HP_MEM_PD Configures whether or not to force power down Internal SRAMx domain. This setting has a lower priority than PMU_FORCE_HP_MEM_PU.
O: No effect
1: Force power down
(R/W)

PMU_FORCE_HP_MEM_NO_ISO Configures whether or not to disable the force isolation of Internal SRAMx domain. This setting has a lower priority than PMU_FORCE_HP_MEM_ISO.
O: No effect
1: Disable
(R/W)

PMU_FORCE_HP_MEM_PU Configures whether or not to force power up Internal SRAMx domain. This setting has a lower priority than PMU_PD_HP_AON_MASK.
O: No effect
1: Force power up
(R/W)
```