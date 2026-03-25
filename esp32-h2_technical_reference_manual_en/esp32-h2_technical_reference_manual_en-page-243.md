

# 6.18 Registers

## 6.18.1 GPIO Matrix Registers

The addresses in this section are relative to GPIO base address provided in Table 4.3-2 in Chapter 4 System and Memory.

### Register 6.1. GPIO_OUT_REG (0x0004)

```
31                                 0
+---------------------------------------------------------------+
|                 0x00000000                | Reset
+---------------------------------------------------------------+

GPIO_OUT_DATA_ORIG Configures the output value of GPIO0 ~ GPIO27 output in simple GPIO output mode.
O: Low level
1: High level

The value of bit0 ~ bit27 correspond to the output value of GPIO0 ~ GPIO27 respectively. Bit28 ~ bit31 are invalid.
(R/W/SC/WTC)
```

### Register 6.2. GPIO_OUT_W1TS_REG (0x0008)

```
31                                 0
+---------------------------------------------------------------+
|                 0x00000000                | Reset
+---------------------------------------------------------------+

GPIO_OUT_W1TS Configures whether or not to set the output register GPIO_OUT_REG of GPIO0 ~ GPIO27.
O: Not set
1: The corresponding bit in GPIO_OUT_REG will be set to 1
Bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid. Recommended operation: use this register to set GPIO_OUT_REG.
(WT)
```