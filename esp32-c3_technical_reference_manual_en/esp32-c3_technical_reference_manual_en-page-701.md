

```markdown
## 28.5.71 Introduction

Figure 28.5-7 shows how I2Cmaster reads data from specified addresses in an I2C slave. I2Cmaster sends two bytes of addresses: the first byte is a 7-bit I2Cslave address followed by a R/W bit, which is 0 and indicates a WRITE; the second byte is I2Cslave’s memory address. After a RSTART condition, I2Cmaster sends the first byte of address again, but the R/W bit is 1 which indicates a READ. Then, I2Cmaster reads data starting from addrM.

## 28.5.7.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. We recommend setting I2C_SLAVE_SCL_STRETCH_EN (slave) to 1, so that SCL can be held low for more processing time when I2Cslave needs to send data. If this bit is not set, software should write data to be sent to I2Cslave’s TX RAM before I2Cmaster initiates transfer. Configuration below is applicable to scenario where I2C_SLAVE_SCL_STRETCH_EN (slave) is 1.
3. Set I2C_FIFO_ADDR_CFG_EN (slave) to 1 to enable double addressing mode.
4. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
5. Configure command registers of I2Cmaster.

| Command registers | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:------------------|:--------|:----------|:--------|:-------------|:---------|
| I2C_COMMANDO (master) | RSTART  | —        | —      | —           | —       |
| I2C_COMMAND1 (master) | WRITE   | 0        | 0      | 1           | 2       |
```