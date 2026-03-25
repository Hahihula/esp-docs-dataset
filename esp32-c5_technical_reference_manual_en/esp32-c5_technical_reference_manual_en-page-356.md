

```markdown
Register 8.29. GPIO_EXT_PAD_COMP_CONFIG_O_REG (0x0058)

31 | [reserved] | 5 | 4 | 2 | 1 | 0
---|------------|----|----|----|----|----
0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 | Reset

GPIO_EXT_XPD_COMP_O Configures whether to enable the function of analog PAD voltage comparator.
O: Disable
1: Enable
(R/W)

GPIO_EXT_MODE_COMP_O Configures the reference voltage for analog PAD voltage comparator.
O: Reference voltage is the internal reference voltage, meanwhile GPIO8 PAD can be used as a regular GPIO
1: Reference voltage is the voltage on the GPIO8 PAD
(R/W)

GPIO_EXT_DREF_COMP_O Configures the internal reference voltage for analog PAD voltage comparator.
O: Internal reference voltage is 0 * VDDPST1
1: Internal reference voltage is 0.1 * VDDPST1
......
6: Internal reference voltage is 0.6 * VDDPST1
7: Internal reference voltage is 0.7 * VDDPST1
(R/W)
```