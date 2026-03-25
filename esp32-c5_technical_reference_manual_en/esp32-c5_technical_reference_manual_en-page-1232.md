

# 34.9 Registers

## 34.9.1 I2C Registers

The addresses in this section are relative to the I2C Controller base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 34.1. I2C_SCL_LOW_PERIOD_REG (0x0000)

```
31                                 9                                 0
+--------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | 0 | Reset |
+--------------------------------------------------------------------------------------------------+
```

**I2C_SCL_LOW_PERIOD** Configures the low level width of the SCL clock in master mode.

Measurement unit: I2C_SCLK clock cycles  
(R/W)

Register 34.2. I2C_SDA_HOLD_REG (0x0030)

```
31                                 9                                 0
+--------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | 0 | Reset |
+--------------------------------------------------------------------------------------------------+
```

**I2C_SDA_HOLD_TIME** Configures the time to hold the data after the falling edge of SCL.

Measurement unit: I2C_SCLK clock cycles  
(R/W)