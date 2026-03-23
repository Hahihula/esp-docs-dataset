

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_EXT_GLITCH_FILTER_CH6_REG             | Glitch Filter configuration register for channel 6                         | 0x0048    | R/W    |
| GPIO_EXT_GLITCH_FILTER_CH7_REG             | Glitch Filter configuration register for channel 7                         | 0x004C    | R/W    |

**ETM Configuration Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_EXT_ETM_EVENT_CHO_CFG_REG             | ETM configuration register for channel 0                                    | 0x0060    | R/W    |
| GPIO_EXT_ETM_EVENT_CH1_CFG_REG             | ETM configuration register for channel 1                                    | 0x0064    | R/W    |
| GPIO_EXT_ETM_EVENT_CH2_CFG_REG             | ETM configuration register for channel 2                                    | 0x0068    | R/W    |
| GPIO_EXT_ETM_EVENT_CH3_CFG_REG             | ETM configuration register for channel 3                                    | 0x006C    | R/W    |
| GPIO_EXT_ETM_EVENT_CH4_CFG_REG             | ETM configuration register for channel 4                                    | 0x0070    | R/W    |
| GPIO_EXT_ETM_EVENT_CH5_CFG_REG             | ETM configuration register for channel 5                                    | 0x0074    | R/W    |
| GPIO_EXT_ETM_EVENT_CH6_CFG_REG             | ETM configuration register for channel 6                                    | 0x0078    | R/W    |
| GPIO_EXT_ETM_EVENT_CH7_CFG_REG             | ETM configuration register for channel 7                                    | 0x007C    | R/W    |
| GPIO_EXT_ETM_TASK_PO_CFG_REG               | GPIO selection register 0 for ETM                                           | 0x00AO    | R/W    |
| GPIO_EXT_ETM_TASK_P1_CFG_REG               | GPIO selection register 1 for ETM                                           | 0x00A4    | R/W    |
| GPIO_EXT_ETM_TASK_P2_CFG_REG               | GPIO selection register 2 for ETM                                           | 0x00A8    | R/W    |
| GPIO_EXT_ETM_TASK_P3_CFG_REG               | GPIO selection register 3 for ETM                                           | 0x00AC    | R/W    |
| GPIO_EXT_ETM_TASK_P4_CFG_REG               | GPIO selection register 4 for ETM                                           | 0x00BO    | R/W    |
| GPIO_EXT_ETM_TASK_P5_CFG_REG               | GPIO selection register 5 for ETM                                           | 0x00B4    | R/W    |
| GPIO_EXT_ETM_TASK_P6_CFG_REG               | GPIO selection register 6 for ETM                                           | 0x00B8    | R/W    |
| GPIO_EXT_ETM_TASK_P7_CFG_REG               | GPIO selection register 7 for ETM                                           | 0x00BC    | R/W    |

**Version Register**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_EXT_VERSION_REG                       | Version control register                                                    | 0x00FC    | R/W    |

## 7.15.4 LP IO MUX Register Summary

The addresses in this section are relative to LP_IO base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **GPIO Configuration/Data Registers**      |                                                                             |           |        |
| LP_IO_OUT_REG                             | LP GPIO output register                                                     | 0x0000    | R/W    |
| LP_IO_OUT_W1TS_REG                         | LP GPIO output set register                                                 | 0x0004    | WT     |
| LP_IO_OUT_W1TC_REG                         | LP GPIO output clear register                                               | 0x0008    | WT     |
| LP_IO_ENABLE_REG                           | LP GPIO output enable register                                              | 0x000C    | R/W    |
| LP_IO_ENABLE_W1TS_REG                      | LP GPIO output enable set register                                          | 0x0010    | WT     |
| LP_IO_ENABLE_W1TC_REG                      | LP GPIO output enable clear register                                        | 0x0014    | WT     |
| LP_IO_STATUS_REG                           | LP GPIO interrupt status register                                           | 0x0018    | R/W    |
| LP_IO_STATUS_W1TS_REG                      | LP GPIO interrupt status set register                                       | 0x001C    | WT     |
| LP_IO_STATUS_W1TC_REG                      | LP GPIO interrupt status clear register                                     | 0x0020    | WT     |
| LP_IO_IN_REG                               | LP GPIO input register                                                      | 0x0024    | RO     |
| LP_IO_PINO_REG                             | LP GPIOO configuration register                                             | 0x0028    | R/W    |
```