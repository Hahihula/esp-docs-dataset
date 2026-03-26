

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.13. GPIO_STRAP_REG (0x0038)

GPIO_STRAPPING Represents the values of GPIO strapping pins.

bit0: GPIO38
bit1: GPIO37
bit2: GPIO36
bit3: GPIO35
bit4: GPIO34
bit5 ~ bit15: invalid

For more information about the functions controlled by strapping pins, see ESP32-P4 Datasheet > Section Strapping Pins. (RO)

Register 9.14. GPIO_IN_REG (0x003C)

GPIO_IN_DATA_NEXT Represents the input value of GPIO0 ~ GPIO31. Each bit represents a pin input value:
0: Low level
1: High level

Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31.
(RO)
```