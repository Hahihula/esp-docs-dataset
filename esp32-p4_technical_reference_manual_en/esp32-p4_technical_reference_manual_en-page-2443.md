

# 45.7 Registers

The addresses in this section are relative to Analog I2C Controller base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program registers that contain reserved fields, please refer to Section Programming Reserved Register Field.

## Register 45.1. ANA_I2C_MST_I2CO_CTRL_REG (0x0000)

```
(reserved)
ANA_I2C_MST_I2CO_BUSY
31 26 25 24
+-----------------------------+
|       0x00000               |
+-----------------------------+
Reset
```

**ANA_I2C_MST_I2CO_CTRL** Configures the transmission information for I2CO.

- Bit[0:7]: Configures the slave address
- Bit[8:15]: Configures the slave register address
- Bit[16:23]: Configures the transmitted data
- Bit[24]: Configures the read or write operation  
  - 0: Write  
  - 1: Read

Once this register is configured, the I2CO master will generate I2C read or write signals. (R/W)

**ANA_I2C_MST_I2CO_BUSY** Represents whether I2CO is currently transferring data.

- 0: I2CO is not transferring data
- 1: I2CO is transferring data  
  (RO)