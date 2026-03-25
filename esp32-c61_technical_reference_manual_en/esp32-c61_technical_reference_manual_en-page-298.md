

```markdown
Register 6.26. IO_MUX_DATE_REG (0x01FC)

| 31 | 28 | 27 | ... | 0 |
|----|----|----|-----|---|
|    |    |    |     |   |
| 0  | 0  | 0  |     | Reset |

IO_MUX_REG_DATE Version control register.
(R/W)

6.19.3 GPIO EXT Registers

The addresses in this section are relative to GPIO EXT base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section VII .

Register 6.27. GPIO_EXT_PAD_COMP_CONFIG_O_REG (0x0058)

| 31 | ... | 5 | 4 | 2 | 1 | 0 |
|----|-----|---|---|---|---|---|
|    |     |   |   |   |   | Reset |

GPIO_EXT_XPD_COMP_O Configures whether to enable the function of Analog Voltage Comparator.
O: Disable
1: Enable
(R/W)

GPIO_EXT_MODE_COMP_O Configures the reference voltage for Analog Voltage Comparator.
O: Reference voltage is the internal reference voltage, meanwhile GPIO8 PAD can be used as a regular GPIO
1: Reference voltage is the voltage on the GPIO8 PAD
(R/W)

GPIO_EXT_DREF_COMP_O Configures the internal reference voltage for Analog Voltage Comparator.
O: Internal reference voltage is 0 * VDDPST1
1: Internal reference voltage is 0.1 * VDDPST1
......
6: Internal reference voltage is 0.6 * VDDPST1
7: Internal reference voltage is 0.7 * VDDPST1
(R/W)
```