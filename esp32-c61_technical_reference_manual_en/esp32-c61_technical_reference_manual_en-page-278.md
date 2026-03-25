

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_EXT_PAD_COMP_FILTER_0_REG             | Zero-crossing detection register                                            | 0x005C    | R/W    |

**ETM Configuration Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_EXT_ETM_EVENT_CHO_CFG_REG             | Configuration register of ETM channel 0                                    | 0x0118    | R/W    |
| GPIO_EXT_ETM_EVENT_CH1_CFG_REG             | Configuration register of ETM channel 1                                    | 0x011C    | R/W    |
| GPIO_EXT_ETM_EVENT_CH2_CFG_REG             | Configuration register of ETM channel 2                                    | 0x0120    | R/W    |
| GPIO_EXT_ETM_EVENT_CH3_CFG_REG             | Configuration register of ETM channel 3                                    | 0x0124    | R/W    |
| GPIO_EXT_ETM_EVENT_CH4_CFG_REG             | Configuration register of ETM channel 4                                    | 0x0128    | R/W    |
| GPIO_EXT_ETM_EVENT_CH5_CFG_REG             | Configuration register of ETM channel 5                                    | 0x012C    | R/W    |
| GPIO_EXT_ETM_EVENT_CH6_CFG_REG             | Configuration register of ETM channel 6                                    | 0x0130    | R/W    |
| GPIO_EXT_ETM_EVENT_CH7_CFG_REG             | Configuration register of ETM channel 7                                    | 0x0134    | R/W    |
| GPIO_EXT_ETM_TASK_PO_CFG_REG               | GPIO selection register 0                                                   | 0x0158    | R/W    |
| GPIO_EXT_ETM_TASK_P1_CFG_REG               | GPIO selection register 1                                                   | 0x015C    | R/W    |
| GPIO_EXT_ETM_TASK_P2_CFG_REG               | GPIO selection register 2                                                   | 0x0160    | R/W    |
| GPIO_EXT_ETM_TASK_P4_CFG_REG               | GPIO selection register 4                                                   | 0x0168    | R/W    |
| GPIO_EXT_ETM_TASK_P5_CFG_REG               | GPIO selection register 5                                                   | 0x016C    | R/W    |

**Interrupt Registers**

| Name                                       | Description                                                                 | Address   | Access     |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|------------|
| GPIO_EXT_INT_RAW_REG                       | GPIO_EXT interrupt raw register                                             | 0x01D0    | RO/WTG/SS  |
| GPIO_EXT_INT_ST_REG                        | GPIO_EXT interrupt masked register                                         | 0x01D4    | RO         |
| GPIO_EXT_INT_ENA_REG                       | GPIO_EXT interrupt enable register                                         | 0x01D8    | R/W        |
| GPIO_EXT_INT_CLR_REG                       | GPIO_EXT interrupt clear register                                          | 0x01DC    | WT         |

**Version Register**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_EXT_VERSION_REG                       | Version control register                                                   | 0x01FC    | R/W    |

## 6.18.4 LP GPIO Matrix Register Summary

The addresses in this section are relative to LP GPIO matrix base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration Registers**                |                                                                             |           |        |
| LP_GPIO_OUT_REG                            | LP_GPIO output register                                                    | 0x0004    | R/W/WT C|
| LP_GPIO_OUT_W1TS_REG                       | LP_GPIO output set register                                                 | 0x0008    | WT     |
| LP_GPIO_OUT_W1TC_REG                       | LP_GPIO output clear register                                               | 0x000C    | WT     |
| LP_GPIO_ENABLE_REG                         | LP_GPIO output enable register                                              | 0x0010    | R/W/WT C|
| LP_GPIO_ENABLE_W1TS_REG                    | LP_GPIO output enable set register                                         | 0x0014    | WT     |
| LP_GPIO_ENABLE_W1TC_REG                    | LP_GPIO output enable clear register                                       | 0x0018    | WT     |
| LP_GPIO_IN_REG                             | LP_GPIO input register                                                     | 0x001C    | RO     |

**Interrupt Status Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LP_GPIO_STATUS_REG                         | LP_GPIO interrupt status register                                          | 0x0020    | R/W/WT C|
| LP_GPIO_STATUS_W1TS_REG                    | LP_GPIO interrupt status set register                                      | 0x0024    | WT     |
| LP_GPIO_STATUS_W1TC_REG                    | LP_GPIO interrupt status clear register                                    | 0x0028    | WT     |
| LP_GPIO_STATUS_NEXT_REG                    | LP_GPIO interrupt source register                                          | 0x002C    | RO     |
```