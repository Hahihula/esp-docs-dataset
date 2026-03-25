

```markdown
30.5.6 I2Cmaster Reads I2Cslave with a 10-bit Address in One Command Sequence

30.5.6.1 Introduction

Figure 30.5-6. I2Cmaster Reading I2Cslave with a 10-bit Address

Figure 30.5-6 shows how I2Cmaster reads data from an I2C slave using 10-bit addressing. Unlike 7-bit addressing, in 10-bit addressing the WRITE command of the I2Cmaster is formed from two bytes, and correspondingly TX RAM of this master stores a 10-bit address of two bytes. The R/W bit in the first byte is 0, which indicates a WRITE operation. After an RSTART condition, I2Cmaster sends the first byte of address again to read data from I2Cslave, but the R/W bit is 1, which indicates a READ operation. The two address bytes can be configured as described in Section 30.5.2.

30.5.6.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. We recommend setting I2C_SLAVE_SCL_STRETCH_EN (slave) to 1, so that SCL can be held low for more processing time when I2Cslave needs to send data. If this bit is not set, the software should write data to be sent to I2Cslave’s TX RAM before I2Cmaster initiates the transfer. The configuration below is applicable to a scenario where I2C_SLAVE_SCL_STRETCH_EN (slave) is 1.
3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command registers of I2Cmaster | op_code | ack_value | ack_exp | ack_check_en | byte_num |
```