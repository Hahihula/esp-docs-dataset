

```markdown
The slave can enable 10-bit addressing by configuring I2C_ADDR_10BIT_EN. I2C_SLAVE_ADDR is used to configure I2C slave address. Specifically, I2C_SLAVE_ADDR[14:7] should be configured as SLV_ADDR[7:0], and I2C_SLAVE_ADDR[6:0] should be configured as (0x78 | SLV_ADDR[9:8]). Since a 10-bit slave address has one more byte than a 7-bit address, byte_num of the WRITE command and the number of bytes in the RAM increase by one. Please refer to Programming Example for detailed descriptions.

When working in slave mode, the I2C controller supports dual address mode, where the first address is the address of an I2C slave, and the second one is the slave's memory address. When using dual address mode, RAM must be accessed in non-FIFO mode. Dual address mode is enabled by setting I2C_FIFO_ADDR_CFG_EN. When the slave address received by the slave is inconsistent with the internally configured slave address, the I2C_SLAVE_ADDR_UNMATCH interrupt will be generated.

## 29.4.13 R/W Bit Check in 10-bit Addressing Mode

In 10-bit addressing mode, when I2C_ADDR_10BIT_RW_CHECK_EN is set to 1, the I2C controller performs a check on the first byte, which consists of slave_addr_first_7bits and a R/W bit. When the R/W bit does not indicate a WRITE operation, i.e. not in line with the I2C protocol, the data transfer ends. If the check feature is not enabled, when the R/W bit does not indicate a WRITE, the data transfer still continues, but transfer failure may occur.

## 29.4.14 To Start the I2C Controller

To start the I2C controller in master mode, after configuring the controller to master mode and command registers, write 1 to I2C_TRANS_START in order to let the master starts to parse and execute command sequences. The master always executes a command sequence starting from command register 0 to a STOP or an END. To execute another command sequence starting from command register 0, refresh commands by writing 1 again to I2C_TRANS_START.

There are two ways to start the I2C controller in slave mode:

* Set I2C_SLV_TX_AUTO_START_EN, and the slave starts automatic transfer upon an address match;
* Clear I2C_SLV_TX_AUTO_START_EN, and always set I2C_TRANS_START before accepting any transfer.

## 29.5 Functional differences between LP_I2C and I2C

LP_I2C can be used as a master to communicate with external devices when the main system sleeps. LP_I2C includes all the functions of the ESP32-C6 I2C_master, but doesn't include any functions of ESP32-C6 I2C_slave. It does not contain any registers related to the I2C_slave. For detailed register list, see 29.10 LP_I2C Register Summary.

The design differences between LP_I2C and I2C master are as follows:

* The size of TX/RX RAM in LP_I2C is 16*8 bit, which means the TXRX FIFO depth is 16 bytes.
* The clock source of APB_CLK in LP_I2C is CLK_AON_FAST. Configure LP_I2C_SCLK_SEL to select the clock source for I2C_SCLK. When LP_I2C_SCLK_SEL is 0, select CLK_ROOT_FAST as clock source, and when LP_I2C_SCLK_SEL is 1, select CLK_XTALD2 as the clock source. Configure LP_EXT_I2CCK_EN high to enable the clock source of I2C_SCLK. Adjust the timing registers accordingly when the clock frequency changes.
```