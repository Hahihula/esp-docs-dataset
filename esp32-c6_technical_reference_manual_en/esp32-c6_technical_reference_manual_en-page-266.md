
```markdown
- Pin Configuration Registers: only GPIO_PINO_REG ~ GPIO_PIN9_REG and GPIO_PIN12_REG ~ GPIO_PIN23_REG are available.
- Input Configuration Registers: can only be configured for GPIO00 ~ GPIO09 and GPIO12 ~ GPIO23.
- Output Configuration Registers: only GPIO_FUNCO_OUT_SEL_CFG_REG ~ GPIO_FUNC9_OUT_SEL_CFG_REG and GPIO_PIN12_OUT_SEL_CFG_REG ~ GPIO_PIN23_OUT_SEL_CFG_REG are available.

| Name                                       | Description                                                                 | Address   | Access  |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|---------|
| Configuration Registers                    |                                                                             |           |         |
| GPIO_OUT_REG                              | GPIO output register                                                        | 0x0004    | R/W/SC/WTC |
| GPIO_OUT_W1TS_REG                          | GPIO output set register                                                    | 0x0008    | WT      |
| GPIO_OUT_W1TC_REG                          | GPIO output clear register                                                  | 0x000C    | WT      |
| GPIO_ENABLE_REG                            | GPIO output enable register                                                 | 0x0020    | R/W/WTC |
| GPIO_ENABLE_W1TS_REG                       | GPIO output enable set register                                             | 0x0024    | WT      |
| GPIO_ENABLE_W1TC_REG                       | GPIO output enable clear register                                           | 0x0028    | WT      |
| GPIO_STRAP_REG                             | Strapping pin register                                                      | 0x0038    | RO      |
| GPIO_IN_REG                                | GPIO input register                                                         | 0x003C    | RO      |
| Interrupt Status Registers                 |                                                                             |           |         |
| GPIO_STATUS_REG                            | GPIO interrupt status register                                               | 0x0044    | R/W/WTC |
| GPIO_STATUS_W1TS_REG                       | GPIO interrupt status set register                                          | 0x0048    | WT      |
| GPIO_STATUS_W1TC_REG                       | GPIO interrupt status clear register                                        | 0x004C    | WT      |
| GPIO_PCPU_INT_REG                          | GPIO CPU interrupt status register                                          | 0x005C    | RO      |
| GPIO_STATUS_NEXT_REG                       | GPIO interrupt source register                                              | 0x014C    | RO      |
| Pin Configuration Registers                |                                                                             |           |         |
| GPIO_PINO_REG                              | GPIO0 configuration register                                                | 0x0074    | R/W     |
| GPIO_PIN1_REG                              | GPIO1 configuration register                                                | 0x0078    | R/W     |
| GPIO_PIN2_REG                              | GPIO2 configuration register                                                | 0x007C    | R/W     |
| ...                                        | ...                                                                         | ...       | ...     |
| GPIO_PIN28_REG                             | GPIO28 configuration register                                               | 0x00E4    | R/W     |
| GPIO_PIN29_REG                             | GPIO29 configuration register                                               | 0x00E8    | R/W     |
| GPIO_PIN30_REG                             | GPIO30 configuration register                                               | 0x00EC    | R/W     |
| Input Configuration Registers              |                                                                             |           |         |
| GPIO_FUNCO_IN_SEL_CFG_REG                  | Configuration register for input signal 0                                   | 0x0154    | R/W     |
| GPIO_FUNC1_IN_SEL_CFG_REG                  | Configuration register for input signal 1                                   | 0x0158    | R/W     |
| GPIO_FUNC2_IN_SEL_CFG_REG                  | Configuration register for input signal 2                                   | 0x015C    | R/W     |
| ...                                        | ...                                                                         | ...       | ...     |
| GPIO_FUNC125_IN_SEL_CFG_REG                | Configuration register for input signal 125                                 | 0x0348    | R/W     |
| GPIO_FUNC126_IN_SEL_CFG_REG                | Configuration register for input signal 126                                 | 0x034C    | R/W     |
| GPIO_FUNC127_IN_SEL_CFG_REG                | Configuration register for input signal 127                                 | 0x0350    | R/W     |
| Output Configuration Registers             |                                                                             |           |         |
| GPIO_FUNCO_OUT_SEL_CFG_REG                 | Configuration register for GPIO0 output                                     | 0x0554    | varies  |
| GPIO_FUNC1_OUT_SEL_CFG_REG                 | Configuration register for GPIO1 output                                     | 0x0558    | varies  |
| GPIO_FUNC2_OUT_SEL_CFG_REG                 | Configuration register for GPIO2 output                                     | 0x055C    | varies  |
| ...                                        | ...                                                                         | ...       | ...     |
```