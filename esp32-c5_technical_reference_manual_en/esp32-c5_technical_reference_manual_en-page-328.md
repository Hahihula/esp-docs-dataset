

```markdown
| Name                     | Description                                                                 | Address   | Access |
|--------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_STRAP_REG           | Strapping pin register                                                      | 0x0000    | RO     |
| GPIO_OUT_REG             | GPIO output register                                                        | 0x0004    | R/W/SC/WTC |
| GPIO_OUT_W1TS_REG        | GPIO output set register                                                    | 0x0008    | WT     |
| GPIO_OUT_W1TC_REG        | GPIO output clear register                                                  | 0x000C    | WT     |
| GPIO_ENABLE_REG          | GPIO output enable register                                                 | 0x0034    | R/W/WTC |
| GPIO_ENABLE_W1TS_REG     | GPIO output enable set register                                             | 0x0038    | WT     |
| GPIO_ENABLE_W1TC_REG     | GPIO output enable clear register                                           | 0x003C    | WT     |
| GPIO_IN_REG              | GPIO input register                                                         | 0x0064    | RO     |
| GPIO_PROCPU_INT_REG      | CPU interrupt status register for GPIO0~GPIO14, GPIO23~GPIO28               | 0x00A4    | RO     |
| GPIO_SDIO_INT_REG        | GPIO_SDIO_INT interrupt status register for GPIO0~GPIO14, GPIO23~GPIO28      | 0x00A8    | RO     |

**Interrupt Status Registers**

| Name                     | Description                                                                 | Address   | Access |
|--------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_STATUS_REG          | GPIO interrupt status register                                              | 0x0074    | R/W/WTC |
| GPIO_STATUS_W1TS_REG     | GPIO interrupt status set register                                          | 0x0078    | WT     |
| GPIO_STATUS_W1TC_REG     | GPIO interrupt status clear register                                        | 0x007C    | WT     |
| GPIO_STATUS_NEXT_REG     | GPIO interrupt source register                                              | 0x00B4    | RO     |

**Pin Configuration Registers**

| Name                     | Description                                                                 | Address   | Access |
|--------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_PIN0_REG            | GPIO0 configuration register                                                | 0x00C4    | R/W    |
| GPIO_PIN1_REG            | GPIO1 configuration register                                                | 0x00C8    | R/W    |
| GPIO_PIN2_REG            | GPIO2 configuration register                                                | 0x00CC    | R/W    |
| GPIO_PIN3_REG            | GPIO3 configuration register                                                | 0x00D0    | R/W    |
| GPIO_PIN4_REG            | GPIO4 configuration register                                                | 0x00D4    | R/W    |
| GPIO_PIN5_REG            | GPIO5 configuration register                                                | 0x00D8    | R/W    |
| GPIO_PIN6_REG            | GPIO6 configuration register                                                | 0x00DC    | R/W    |
| GPIO_PIN7_REG            | GPIO7 configuration register                                                | 0x00E0    | R/W    |
| GPIO_PIN8_REG            | GPIO8 configuration register                                                | 0x00E4    | R/W    |
| GPIO_PIN9_REG            | GPIO9 configuration register                                                | 0x00E8    | R/W    |
| GPIO_PIN10_REG           | GPIO10 configuration register                                               | 0x00EC    | R/W    |
| GPIO_PIN11_REG           | GPIO11 configuration register                                               | 0x00F0    | R/W    |
| GPIO_PIN12_REG           | GPIO12 configuration register                                               | 0x00F4    | R/W    |
| GPIO_PIN13_REG           | GPIO13 configuration register                                               | 0x00F8    | R/W    |
| GPIO_PIN14_REG           | GPIO14 configuration register                                               | 0x00FC    | R/W    |
| GPIO_PIN23_REG           | GPIO23 configuration register                                               | 0x0120    | R/W    |
| GPIO_PIN24_REG           | GPIO24 configuration register                                               | 0x0124    | R/W    |
| GPIO_PIN25_REG           | GPIO25 configuration register                                               | 0x0128    | R/W    |
| GPIO_PIN26_REG           | GPIO26 configuration register                                               | 0x012C    | R/W    |
| GPIO_PIN27_REG           | GPIO27 configuration register                                               | 0x0130    | R/W    |
| GPIO_PIN28_REG           | GPIO28 configuration register                                               | 0x0134    | R/W    |

**Input Configuration Registers**

| Name                     | Description                                                                 | Address   | Access |
|--------------------------|-----------------------------------------------------------------------------|-----------|--------|
| GPIO_FUNC6_IN_SEL_CFG_REG | Configuration register for input signal 6                                   | 0x02DC    | R/W    |
| GPIO_FUNC7_IN_SEL_CFG_REG | Configuration register for input signal 7                                   | 0x02E0    | R/W    |
| GPIO_FUNC8_IN_SEL_CFG_REG | Configuration register for input signal 8                                   | 0x02E4    | R/W    |
```