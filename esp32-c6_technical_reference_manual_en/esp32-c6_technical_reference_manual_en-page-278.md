

```markdown
Register 7.13. GPIO_PINn_REG (n: 0-30) (0x0074+4*n)

Continued from the previous page...

GPIO_PINn_INT_ENA Configures whether or not to enable CPU interrupt or CPU non-maskable interrupt.

*   bit13: Configures whether or not to enable CPU interrupt:
    *   0: Disable
    *   1: Enable
*   bit14: Configures CPU non-maskable interrupt:
    *   0: Disable
    *   1: Enable
*   bit15 ~ bit17: invalid

(R/W)

Register 7.14. GPIO_STATUS_NEXT_REG (0x014C)
```

```markdown
31                                 0
+----------------------------------------------------------+
|                0x0000000               |Reset|
+----------------------------------------------------------+

GPIO_STATUS_INTERRUPT_NEXT Represents the interrupt source signal of GPIO0 ~ GPIO30.
Bit0 ~ bit30 are corresponding to GPIO0 ~ 30. Bit31 is invalid. Each bit represents:
*   0: The GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
*   1: The GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE.

The interrupt could be rising edge interrupt, falling edge interrupt, level sensitive interrupt and any edge interrupt.

(RO)
```