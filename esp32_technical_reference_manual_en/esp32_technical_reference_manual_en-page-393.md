Title: Chapter 21 I2C Controller (I2C)

Subtitle: GoBack

Section Title: 21.3.5 I2C Master Writes to Slave

Figure Caption:
- Figure 21.3.5 - I2C Master Writes to Slave with 7-bit Address

Body Text:

In all subsequent figures that illustrate I2C transactions and behavior, both the I2C Master and Slave devices are assumed to be ESP32 I2C peripheral controllers for ease of demonstration.

Figure Caption:
- Figure 21.3-5 shows the I2C Master writing N bytes of data to an I2C Slave. According to the I2C protocol, the first byte is the Slave address. As shown in the diagram, the first byte of the RAM unit has been populated with the Slave's 7-bit address plus the 1-bit read/write flag. In this case, the flag is zero, indicating a write operation.

The rest of the RAM unit holds N bytes of data ready for transmission. The cmd unit has been populated with the sequence of commands for the operation.
For the I2C master to begin an operation, the bus must not be busy, i.e., the SCL line must not be pulled low by another device on the I2C bus.

The following text continues but is cut off and cannot be transcribed in full. The content discusses various aspects of how data transmission works between a Master and Slave using the I2C protocol with specific details about interrupt handling, check value verification during write operations to ensure correct address matching before proceeding further into writing or reading processes on RAM.

Footer:
- Espresso Systems
- 393 ESP32 TRM (Version 5.6)
- Submit Documentation Feedback