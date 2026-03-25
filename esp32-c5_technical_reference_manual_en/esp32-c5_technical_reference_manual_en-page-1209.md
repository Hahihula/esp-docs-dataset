

```markdown
Chapter 34 I2C Controller (I2C)

The slave can enable 10-bit addressing by configuring `I2C_ADDR_10BIT_EN`. `I2C_SLAVE_ADDR` is used to configure I2C slave address. Specifically, `I2C_SLAVE_ADDR[14:7]` should be configured as SILV_ADDR[7:0], and `I2C_SLAVE_ADDR[6:0]` should be configured as (0x78 | SLV_ADDR[9:8]). Since a 10-bit slave address has one more byte than a 7-bit address, `byte_num` of the WRITE command and the number of bytes in the RAM increase by one. Please refer to Programming Example for detailed descriptions.

When working in slave mode, the I2C controller supports dual address mode, where the first address is the address of an I2C slave, and the second one is the slave's memory address. When using dual address mode, RAM must be accessed in non-FIFO mode.

Dual address mode is enabled by setting `I2C_FIFO_ADDR_CFG_EN`. When the slave address received by the slave is inconsistent with the internally configured slave address, the I2C_SLAVE_ADDR_UNMATCH interrupt will be generated.

34.4.13 R/W Bit Check in 10-bit Addressing Mode

In 10-bit addressing mode, when `I2C_ADDR_10BIT_RW_CHECK_EN` is set to 1, the I2C controller performs a check on the first byte, which consists of slave_addr_first_7bits and a R/W bit. When the R/W bit does not indicate a WRITE operation, i.e., not in line with the I2C protocol, the data transfer ends. If the check feature is not enabled, when the R/W bit does not indicate a WRITE, the data transfer still continues, but transfer failure may occur.

34.4.14 Start the I2C Controller

To start the I2C controller in master mode, after configuring the controller to master mode and command registers, write 1 to `I2C_TRANS_START` in order to let the master start to parse and execute command sequences. The master always executes a command sequence starting from the command register 0 to a STOP or an END. To execute another command sequence starting from command register 0, refresh commands by writing 1 again to `I2C_TRANS_START`.

To start the I2C controller slave mode, after configuring the controller to slave mode and setting the relevant registers, write 1 to `I2C_TRANS_START`. The slave will respond to the master when the received address matches.

For the slave device, please note:

- Always set `I2C_TRANS_START` before accepting any transfer. Otherwise, even if the address matches, the slave will not respond to the master.
- If the master initiates a STOP condition and prematurely terminates the transmission with the slave, the slave must first set `I2C_SLV_TX_AUTO_START_EN`, then set `I2C_TRANS_START`, and finally clear `I2C_SLV_TX_AUTO_START_EN` before the next transfer. Otherwise, an abnormal TX FIFO pointer issue will occur in the slave.

34.5 Functional Differences Between LP_I2C and I2C

LP_I2C can be used as a master to communicate with external devices when the main system sleeps. LP_I2C includes all the functions of the ESP32-C5 `I2C_master`, but doesn't include any functions of ESP32-C5 `I2C_slave`. It does not contain any registers related to the `I2C_slave`. For detailed register list, see 34.8.2 LP_I2C Register Summary.
```