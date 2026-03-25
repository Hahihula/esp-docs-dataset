

# 30.8 Registers

The addresses in this section are relative to I2C Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

## Register 30.1. I2C_SCL_LOW_PERIOD_REG (0x0000)

```
31                                 9        8         0
+-----------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
+-----------------------------------------------+
```

**I2C_SCL_LOW_PERIOD** Configures the low level width of the SCL Clock in Master mode.  
Measurement unit: I2C_SCLK  
(R/W)

## Register 30.2. I2C_SDA_HOLD_REG (0x0030)

```
31                                 9        8         0
+-----------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
+-----------------------------------------------+
```

**I2C_SDA_HOLD_TIME** Configures the time to hold the data after the falling edge of SCL.  
Measurement unit: I2C_SCLK  
(R/W)

## Register 30.3. I2C_SDA_SAMPLE_REG (0x0034)

```
31                                 9        8         0
+-----------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
+-----------------------------------------------+
```

**I2C_SDA_SAMPLE_TIME** Configures the time for sampling SDA.  
Measurement unit: I2C_SCLK  
(R/W)