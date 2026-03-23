

```markdown
Chapter 28 I2C Controller (I2C)  
GoBack

28.4.13 R/W Bit Check in 10-bit Addressing Mode  
In 10-bit addressing mode, when `I2C_ADDR_10BIT_RW_CHECK_EN` is set to 1, the I2C controller performs a check on the first byte, which consists of `slave_addr_first_7bits` and a R/W bit. When the R/W bit does not indicate a WRITE operation, i.e. not in line with the I2C protocol, the data transfer ends. If the check feature is not enabled, when the R/W bit does not indicate a WRITE, the data transfer still continues, but transfer failure may occur.

28.4.14 To Start the I2C Controller  
To start the I2C controller in master mode, after configuring the controller to master mode and command registers, write 1 to `I2C_TRANS_START` in order that the master starts to parse and execute command sequences. The master always executes a command sequence starting from command register 0 to a STOP or an END at the end. To execute another command sequence starting from command register 0, refresh commands by writing 1 again to `I2C_TRANS_START`.  
To start the I2C controller in slave mode, there are two ways:  
• Set `I2C_SLV_TX_AUTO_START_EN`, and the slave starts automatic transfer upon an address match;  
• Clear `I2C_SLV_TX_AUTO_START_EN`, and always set `I2C_TRANS_START` before transfer.

28.5 Programming Example  
This sections provides programming examples for typical communication scenarios. ESP32-C3 has one I2C controller. For the convenience of description, I2C masters and slaves in all subsequent figures are ESP32-C3 I2C controllers. I2C master is referred to as `I2Cmaster`, and I2C slave is referred to as `I2Cslave`.

28.5.1 I2Cmaster Writes to I2Cslave with a 7-bit Address in One Command Sequence
```