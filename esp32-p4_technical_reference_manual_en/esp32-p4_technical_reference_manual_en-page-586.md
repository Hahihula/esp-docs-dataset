

```markdown
Chapter 9 GPIO Matrix and IO MUX



Register 9.15. GPIO_IN1_REG (0x0040)

| 31 | 25 | 24 | GPO_IN1_DATA_NEXT |
|----:|----:|----:|-------------------|
|    |    |    |                   |
| 0x00000           | Reset |

GPIO_IN1_DATA_NEXT Represents the input value of GPIO32 ~ GPIO54. Each bit represents a pin input value:
O: Low level
1: High level
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54.
(RO)



Register 9.16. GPIO_STATUS_REG (0x0044)

| 31 | GPO_STATUS_INTERRUPT |
|----:|----------------------|
|    |                      |
| 0x000000           | Reset |

GPIO_STATUS_INTERRUPT The interrupt status of GPIO0 ~ GPIO31, can be configured by the software.
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31.
Each bit represents the status of its corresponding GPIO:
O: Represents the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE, or this bit is configured to 0 by the software.
1: Represents the GPIO generates the interrupt configured by GPIO_PINn_INT_TYPE, or this bit is configured to 1 by the software.
(R/W/WTC)
```