

```markdown
Register 8.11. GPIO_STATUS_REG (0x0074)

31                                 0
+----------------------------------------------------------+
|                0x000000               |Reset|
+----------------------------------------------------------+

GPIO_STATUS_INTERRUPT The interrupt status of GPIO0~GPIO14 and GPIO23~GPIO28, can be configured by the software.
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28. Each bit represents the status of its corresponding GPIO:
- 0: Represents the GPIO does not generate the interrupt configured by `GPIO_PINn_INT_TYPE`, or this bit is configured to 0 by the software.
- 1: Represents the GPIO generates the interrupt configured by `GPIO_PINn_INT_TYPE`, or this bit is configured to 1 by the software. (R/W/WTC)

Register 8.12. GPIO_STATUS_W1TS_REG (0x0078)

31                                 0
+----------------------------------------------------------+
|                0x000000               |Reset|
+----------------------------------------------------------+

GPIO_STATUS_W1TS Configures whether or not to set the interrupt status register `GPIO_STATUS_INTERRUPT` of GPIO0~GPIO14 and GPIO23~GPIO28.
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.

The value of each bit can be:
0: Not set
1: The corresponding bit in `GPIO_STATUS_INTERRUPT` will be set to 1.
Recommended operation: use this register to set `GPIO_STATUS_INTERRUPT`. (WT)
```