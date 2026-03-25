

```markdown
## 6.19.1 HP GPIO Matrix Registers

The addresses in this section are relative to HP GPIO matrix base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section VII .

### Register 6.1. GPIO_STRAP_REG (0x0000)

```text
(reserved)
31                                 16                                  0
+---------------------------------------------------------------+
|                 0x00                |         Reset        |
+---------------------------------------------------------------+
```

**GPIO_STRAPPING** Represents the values of GPIO strapping pins.

- Bit[0]: invalid
- Bit[1]: invalid
- Bit[2]: GPIO8
- Bit[3]: GPIO9
- Bit[4]: GPIO7
- Bit[5]~Bit[15]: Invalid

For more information about the functions controlled by strapping pins, see Chapter 8 Chip Boot Control.

(RO)

### Register 6.2. GPIO_OUT_REG (0x0004)

```text
31                                 0
+---------------------------------------+
|               0x000000              | Reset
+---------------------------------------+
```

**GPIO_OUT_DATA_ORIG** Configures the output value of GPIO0~GPIO13 and GPIO22~GPIO29 in simple GPIO output mode.

0: Low level  
1: High level

The value of bit[0]~bit[13] and bit[22]~bit[29] corresponds to the output value of GPIO0~GPIO13 and GPIO22~GPIO29 respectively.

(R/W/SC/WTC)
```