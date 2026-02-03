**Title:**
Chapter 27 I2C Controller (I2C)

**Menu:**
GoBack

**Subtitle:**
Register 2718. I2C_SCL_STRETCH_CONF_REG (0x0084)

**Table Description:**
- The table shows the register layout for "I2C_SCL_STRETCH_CONF_REG" with various fields such as "I2C_SLAVE_BYTE_ACK_WL", "I2C_SLAVE_BYTE ACK OWL", etc.
- Each field is labeled and has a corresponding bit position in hexadecimal format.

**Body Text:**

1. **Field Description - I2C_STRETCH_PROTECT_NUM**
   - Configures the time period to release the SCL line from stretching to avoid timing violation. Usually it should be larger than the SDA start up time.
   - Access type (R/W)

2. **Field Description - I2C_SCL_SCL_STRETCH_EN**
   - The enable bit for SCL clock stretching: 0: Disable; 1: Enable
   - When this is enabled, one of the four events will be stretched low when "I2C_SLAVE_SCL_STRETCH_EN" is set to high.
   - Access type (R/W)

3. **Field Description - I2C_SCL_SCL_STRETCH_CLR**
   - Set this bit to clear SCL clock stretching.

4. **Field Description - I2C_SLAVE_BYTE_ACKCTL_EN**
   - The enable bit for slave to control the level of the ACK bit.
   - Access type (R/W)

5. **Field Description - I2C_SLAVE_BYTE_ACK_LVL**
   - Set the level of the ACK bit when "I2C_SLAVE_BYTE_ACK_CTL_EN" is set.

**Footer:**
Espressif Systems
1026 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback