

```markdown
| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| IO_MUX_GPIO23_REG                    | IO MUX configuration register for GPIO23                                   | 0x0060    | R/W    |
| IO_MUX_GPIO24_REG                    | IO MUX configuration register for GPIO24                                   | 0x0064    | R/W    |
| IO_MUX_GPIO25_REG                    | IO MUX configuration register for GPIO25                                   | 0x0068    | R/W    |
| IO_MUX_GPIO26_REG                    | IO MUX configuration register for GPIO26                                   | 0x006C    | R/W    |
| IO_MUX_GPIO27_REG                    | IO MUX configuration register for GPIO27                                   | 0x0070    | R/W    |
| IO_MUX_GPIO28_REG                    | IO MUX configuration register for GPIO28                                   | 0x0074    | R/W    |
| IO_MUX_GPIO29_REG                    | IO MUX configuration register for GPIO29                                   | 0x0078    | R/W    |
| IO_MUX_GPIO30_REG                    | IO MUX configuration register for GPIO30                                   | 0x007C    | R/W    |
| Version Register                     |                                                                               |           |        |
| IO_MX_DATE_REG                       | Version control register                                                     | 0x00FC    | R/W    |

### 7.15.3 GPIO_EXT Register Summary

GPIO_EXT registers consist of SDM registers, Glitch Filter registers, and ETM registers.

The addresses in this section are relative to (GPIO base address + 0x0F00). GPIO base address is provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **SDM Configure Registers**                |                                                                             |           |        |
| GPIO_EXT_SIGMADELTA0_REG                   | Duty cycle configuration register for SDM channel 0                        | 0x0000    | R/W    |
| GPIO_EXT_SIGMADELTA1_REG                   | Duty cycle configuration register for SDM channel 1                        | 0x0004    | R/W    |
| GPIO_EXT_SIGMADELTA2_REG                   | Duty cycle configuration register for SDM channel 2                        | 0x0008    | R/W    |
| GPIO_EXT_SIGMADELTA3_REG                   | Duty cycle configuration register for SDM channel 3                        | 0x000C    | R/W    |
| GPIO_EXT_SIGMADELTA_MISC_REG               | MISC register                                                               | 0x0024    | R/W    |
| **Glitch Filter Configuration Registers**  |                                                                             |           |        |
| GPIO_EXT_GLITCH_FILTER_CH0_REG             | Glitch Filter configuration register for channel 0                         | 0x0030    | R/W    |
| GPIO_EXT_GLITCH_FILTER_CH1_REG             | Glitch Filter configuration register for channel 1                         | 0x0034    | R/W    |
| GPIO_EXT_GLITCH_FILTER_CH2_REG             | Glitch Filter configuration register for channel 2                         | 0x0038    | R/W    |
| GPIO_EXT_GLITCH_FILTER_CH3_REG             | Glitch Filter configuration register for channel 3                         | 0x003C    | R/W    |
| GPIO_EXT_GLITCH_FILTER_CH4_REG             | Glitch Filter configuration register for channel 4                         | 0x0040    | R/W    |
| GPIO_EXT_GLITCH_FILTER_CH5_REG             | Glitch Filter configuration register for channel 5                         | 0x0044    | R/W    |
```