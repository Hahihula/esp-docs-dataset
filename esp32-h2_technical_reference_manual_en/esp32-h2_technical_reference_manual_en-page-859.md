

```markdown
## 30.5.5.1 Introduction

Figure 30.5-5 shows how I2Cmaster reads N bytes of data from an I2C slave using 7-bit addressing. cmd1 is a WRITE command. When cmd1 is executed, I2Cmaster sends the address of I2Cslave. The byte sent comprises a 7-bit I2Cslave address and a R/W bit. When the R/W bit is 1, it indicates a READ operation. If the address of an I2C slave matches the sent address, this matching slave starts sending data to I2Cmaster. I2Cmaster generates acknowledgments according to ack_value defined in the READ command upon receiving a byte.

As illustrated in Figure 30.5-5, I2Cmaster executes two READ commands: it generates ACKs for (N-1) bytes of data in cmd2, and a NACK for the last byte of data in cmd 3. This configuration may be changed as required. I2Cmaster writes received data into the controller RAM from addr0, whose original content (the address of I2Cslave and a R/W bit) is overwritten by byte0 marked red in Figure 30.5-5.

## 30.5.5.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. It is recommended to set I2C_SLAVE_SCL_STRETCH_EN (slave) to 1, so that SCL can be held low for more processing time when I2Cslave needs to send data. If this bit is not set, the software should write data to be sent to I2Cslave’s TX RAM before I2Cmaster initiates the transfer. The configuration below is applicable to the scenario where I2C_SLAVE_SCL_STRETCH_EN (slave) is 1.
3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command | registers of | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|---------|--------------|---------|-----------|---------|--------------|----------|
| I2Cmaster |              |         |           |         |              |          |
```