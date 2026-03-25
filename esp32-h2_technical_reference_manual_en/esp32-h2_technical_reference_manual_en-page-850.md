

```markdown
The slave can enable 10-bit addressing by configuring I2C_ADDR_10BIT_EN. I2C_SLAVE_ADDR is used to configure I2C slave address. Specifically, I2C_SLAVE_ADDR[14:7] should be configured as SLV_ADDR[7:0], and I2C_SLAVE_ADDR[6:0] should be configured as (0x78 | SLV_ADDR[9:8]). Since a 10-bit slave address has one more byte than a 7-bit address, byte_num of the WRITE command and the number of bytes in the RAM increase by one. Please refer to Programming Example for detailed descriptions.

When working in slave mode, the I2C controller supports dual address mode, where the first address is the address of an I2C slave, and the second one is the slave's memory address. When using dual address mode, RAM must be accessed in non-FIFO mode. Dual address mode is enabled by setting I2C_FIFO_ADDR_CFG_EN. When the slave address received by the slave is inconsistent with the internally configured slave address, the I2C_SLAVE_ADDR_UNMATCH interrupt will be generated.

### 30.4.13 R/W Bit Check in 10-bit Addressing Mode

In 10-bit addressing mode, when I2C_ADDR_10BIT_RW_CHECK_EN is set to 1, the I2C controller performs a check on the first byte, which consists of slave_addr_first_7bits and a R/W bit. When the R/W bit does not indicate a WRITE operation, i.e., not in line with the I2C protocol, the data transfer ends. If the check feature is not enabled, when the R/W bit does not indicate a WRITE, the data transfer still continues, but transmission errors may occur.

### 30.4.14 To Start the I2C Controller

To start the I2C controller in master mode, after configuring the controller to master mode and command registers, write 1 to I2C_TRANS_START in order to let the master starts to parse and execute command sequences. The master always executes a command sequence starting from the command register 0 to a STOP or an END. To execute another command sequence starting from command register 0, refresh commands by writing 1 again to I2C_TRANS_START.

There are two ways to start the I2C controller in slave mode:

*   Set I2C_SLV_TX_AUTO_START_EN, and the slave starts automatic transfer upon an address match.
*   Clear I2C_SLV_TX_AUTO_START_EN, and always set I2C_TRANS_START before accepting any transfer.

## 30.5 Programming Example

This section provides programming examples for typical communication scenarios. ESP32-H2 has two I2C controllers. For the convenience of description, I2C masters and slaves in all subsequent figures are ESP32-H2 I2C controllers. I2C master is referred to as I2C_master, and I2C slave is referred to as I2C_slave.

### 30.5.1 I2C_master Writes to I2C_slave with a 7-bit Address in One Command Sequence
```