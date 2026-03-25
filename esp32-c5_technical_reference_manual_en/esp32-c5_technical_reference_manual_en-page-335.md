

```markdown
Chapter 8 GPIO Matrix and IO MUX

Register 8.1. GPIO_STRAP_REG (0x0000)

GPIO_STRAPPING Represents the values of GPIO strapping pins.
- Bit[0]: GPIO26
- Bit[1]: MTMS
- Bit[2]: MTDI
- Bit[3]: GPIO27
- Bit[4]: GPIO28
- Bit[5]: GPIO7
- Bit[6]: GPIO25
- Bit[7]~bit[15]: Invalid

For more information about the functions controlled by strapping pins, see Chapter 10 Chip Boot Control.
(RO)

Register 8.2. GPIO_OUT_REG (0x0004)

GPIO_OUT_DATA_ORIG Configures the output value of GPIO0~GPIO14 and GPIO23~GPIO28 output in simple GPIO output mode.
0: Low level
1: High level

The value of bit[0]~bit[14] and bit[23]~bit[28] corresponds to the output value of GPIO0~GPIO14 and GPIO23~GPIO28 respectively.
(R/W/SC/WTC)
```