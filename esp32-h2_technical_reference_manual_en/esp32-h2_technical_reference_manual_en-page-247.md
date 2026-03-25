

```markdown
Register 6.9. GPIO_STATUS_REG (0x0044)

31                                 0
+-----------------------------------------------+
|                0x000000               |Reset
+-----------------------------------------------+

GPIO_STATUS_INTERRUPT The interrupt status of GPIO0 ~ GPIO27, can be configured by the software.

- Bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid.
- Each bit represents the status of its corresponding GPIO:
  - 0: Represents the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE, or this bit is configured to 0 by the software.
  - 1: Represents the GPIO generates the interrupt configured by GPIO_PINn_INT_TYPE, or this bit is configured to 1 by the software.

(R/W/WTC)

Register 6.10. GPIO_STATUS_W1TS_REG (0x0048)

31                                 0
+-----------------------------------------------+
|                0x000000               |Reset
+-----------------------------------------------+

GPIO_STATUS_W1TS Configures whether or not to set the interrupt status register GPIO_STATUS_INTERRUPT of GPIO0 ~ GPIO27.

- Bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid.
- If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be set to 1.
- Recommended operation: use this register to set GPIO_STATUS_INTERRUPT.

(WT)
```