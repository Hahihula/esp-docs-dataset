

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.19. GPIO_STATUS1_REG (0x0050)

GPIO_STATUS1_INTERRUPT The interrupt status of GPIO32 ~ GPIO54, can be configured by the software.

Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54.
Each bit represents the status of its corresponding GPIO:
0: Represents the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE, or this bit is configured to 0 by the software.
1: Represents the GPIO generates the interrupt configured by GPIO_PINn_INT_TYPE, or this bit is configured to 1 by the software.

Register 9.20. GPIO_STATUS1_W1TS_REG (0x0054)

GPIO_STATUS1_W1TS Configures whether or not to set the interrupt status register GPIO_STATUS1_INTERRUPT of GPIO32 ~ GPIO54.
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54.
If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS1_INTERRUPT will be set to 1.

Recommended operation: use this register to set GPIO_STATUS1_INTERRUPT. (WT)
```