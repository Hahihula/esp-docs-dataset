

# 44.9 Registers

## 44.9.1 I2C Registers

The addresses in this section are relative to the I2C Controller base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 44.1. I2C_SCL_LOW_PERIOD_REG (0x0000)

```
(reserved)
I2C_SCL_LOW_PERIOD
31                                 9                                  0
+-----------------------------------------------+
|                                         | Reset |
+-----------------------------------------------+
```

**I2C_SCL_LOW_PERIOD** Configures the low level width of the SCL Clock in master mode.

Measurement unit: I2C_SCLK clock cycles  
(R/W)

---

### Register 44.2. I2C_SDA_HOLD_REG (0x0030)

```
(reserved)
I2C_SDA_HOLD_TIME
31                                 9                                  0
+-----------------------------------------------+
|                                         | Reset |
+-----------------------------------------------+
```

**I2C_SDA_HOLD_TIME** Configures the time to hold the data after the falling edge of SCL.

Measurement unit: I2C_SCLK clock cycles  
(R/W)