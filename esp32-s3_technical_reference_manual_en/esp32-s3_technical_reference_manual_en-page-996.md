**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Section Titles and Content:**

1. **27.4.13 R/W Bit Check in 10-bit Addressing Mode**
   - In a 10-bit addressing mode, when `I2C_ADDR_10BIT_RW_CHECK_EN` is set to 1, the I2C controller performs a check on the first byte which consists of slave_addr_first_7bits and an R/W bit. When the R/W bit does not indicate a WRITE operation (i.e., out of line with the I2C protocol), data transfer ends.
   - If this feature is not enabled, when the `R/W` bit indicates no WRITE action but continues to perform transfers; however, failure may occur.

2. **27.4.14 To Start the I2C Controller**
   - In master mode:
     1. After configuring the controller for master mode and command registers, write '1' to `I2CTrans_Start` in order that the master starts parsing commands.
     2. The master always executes a command sequence starting from command register O or STOP at the end of an END operation.

   - In slave mode:
     1. To start with automatic transfer upon address match, set `I2C_SLV_TX_AUTO_START_EN`.
     2. Clear `I2C_SLV_TX_AUTO_START_EN` and always ensure that `I2C_Trans_Start` is enabled before any transfers.
   
3. **27.5 Programming Example**
   - This section provides programming examples for typical communication scenarios involving ESP32-S3 with one I2C controller.

4. **27.5.1 I2Cmaster Writes to I2CSlave with a 7-bit Address in One Command Sequence**

**Footer:**
- Page number and document version information:
  - "996"
  - "ESP32-S3 TRM (Version 1.7)"
  
**Navigation Links:**
- GoBack
- Submit Documentation Feedback

**Company Information:**
- Espressif Systems