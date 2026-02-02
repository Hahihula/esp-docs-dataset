Title: Chapter 21 I2C Controller (I2C)

Body Text:
detecting the interrupt, software will get the starting and ending addresses in the RAM by reading RXFIFO_START_ADDR and RXFIFO_END_ADDR bits in register RXFIFO_ST_REG, and fetch the data for further processing. Register RXFIFO_START_ADDR is refreshed only once during each transmission, while RXFIFO_END_ADDR gets refreshed every time when either I2C_RX_REC_FULL_INT or I2CTransComplete_INT interrupt is generated.

When the END command is not used, the I2C master can transmit up to (14\*255-1) bytes of valid data, and the cmd unit is populated with RSTART + 14 WRITE + 1 STOP.

There are several special cases to be noted:
- If the Master fails to send a STOP bit, because the SDA is pulled low by other devices, then the Master needs to be reset.
- If the Master fails to send a START bit, because the SDA or SCL is pulled low by other devices, then the Master needs to be reset. It is recommended that the software uses a timeout period to implement the reset.

If the SDA is pulled low by the Slave during transmission, the Master can simply release it by sending nine SCL clock signals at the most.

It is important to note that the behaviour of another I2C master or slave device on the bus may not always be similar to that of the ESP32 I2C peripheral in the master- or slave-mode operation described above. Please consult the datasheets of the respective I2C devices to ensure proper operation under all bus conditions.

The ESP32 I2C controller uses 7-bit addressing by default. However, 10-bit addressing can also be used. In the master, this is done by sending a second I2C address byte after the first address byte. In the slave, the I2C_SLAVE_ADDR_10BIT_EN bit in I2C_SLAVE_ADDR_REG can be set to activate a 10-bit addressing mode.

I2C_SLAVE_ADDR is used to configure the I2C Slave address, as per usual. Figure 21.3-6 shows the equivalent of I2C Master operation writing N-bytes of data to an I2C Slave with a 10-bit address. Since 10-bit Slave addresses require an extra address byte, both the byte_num field of the WRITE command and the number of total bytes in RAM increase by one.

Figure Caption:
Figure 21.3-6. I2C Master Writes to Slave with 10-bit Address

Footer Text (Left):
Espressif Systems
Page Number: 394
Document Version Information: ESP32 TRM (Version 5.6)

Footer Link/Action Button (Right): Submit Documentation Feedback