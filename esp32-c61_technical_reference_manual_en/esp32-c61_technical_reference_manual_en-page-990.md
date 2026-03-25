

```markdown
## 27.6.7.1 Introduction

Figure 27.6-7 shows how I2Cmaster reads data from specified addresses in an I2C slave. I2Cmaster sends two bytes of addresses: the first byte is a 7-bit I2Cslave address followed by a R/W bit, which is 0 and indicates a WRITE; the second byte is I2Cslave’s memory address. After a RSTART condition, I2Cmaster sends the first byte of address again, but the R/W bit is 1 which indicates a READ. Then, I2Cmaster reads data starting from addrM.

When double addressing mode is used, the slave RAM must be accessed in non-FIFO mode, and clock stretching by the slave must be disabled. In this configuration, the slave’s TX FIFO operates in a non-FIFO manner. Even in the case of an underflow condition where the master attempts to read more data than available, the slave continues to return data corresponding to the current address pointer without generating warnings. The address pointer wraps around to the beginning of the memory space once the end is reached.

## 27.6.7.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. We recommend setting I2C_SLAVE_SCL_STRETCH_EN (slave) to 1, so that SCL can be held low for more processing time when I2Cslave needs to send data. If this bit is not set, the software should write data to be sent to I2Cslave’s TX RAM before I2Cmaster initiates the transfer. The configuration below is applicable to the scenario where I2C_SLAVE_SCL_STRETCH_EN (slave) is 1.
3. Set I2C_FIFO_ADDR_CFG_EN (slave) to 1 to enable dual address mode.
4. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
5. Configure command registers of I2Cmaster.
```