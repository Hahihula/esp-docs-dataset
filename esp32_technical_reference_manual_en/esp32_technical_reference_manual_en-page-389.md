**Title:**
Chapter 21 I2C Controller (I2C)

**Subtitle: Overview**

**Body Text:**
An I2C (Inter-Integrated Circuit) bus can be used for communication with several external devices connected to the same bus as ESP32. The ESP32 has dedicated hardware to communicate with peripherals on the I2C bus.

**Subtitle: Features**

**List of features under "Features":**
- Supports both master mode and slave mode
- Supports multi-master and multi-slave communication
- Supports standard mode (100 kbit/s)
- Supports fast mode (400 kbit/s)
- Supports 7-bit addressing and 10-bit addressing
- Supports continuous data transmission with disabled Serial Clock Line (SCL)
- Supports programmable digital noise filter

**Subtitle: Functional Description**

**Sub-subtitle: Introduction**

**Body Text under "Introduction":**
I2C is a two-wire bus, consisting of an SDA and an SCL line. These lines are configured to open the drain output. The lines are shared by two or more devices: usually one or more masters and one or more slaves.

Communication starts when a master sends out a start condition: it will pull the SDA line low, and then will pull the SCL line high. It will send out nine clock pulses over the SCL line. The first eight pulses are used to shift out a byte consisting of a 7-bit address and a read/write bit. If a slave with this address is active on the bus, the slave can answer by pulling the SDA low on the ninth clock pulse. The master can then send out more 9-bit clock pulse clusters and, depending on the read/write bit sent, the device or the master will shift out data on the SDA line, with the other side acknowledging the transfer by pulling the SDA low on the ninth clock pulse.

During data transfer, the SDA line changes only when the SCL line is low. When the master has finished the communication, it will send a stop condition on the bus by raising SDA, while SCL will already be high.

The ESP32 I2C peripheral can handle the I2C protocol, freeing up the processor cores for other tasks.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version Information:** 
ESP32 TRM (Version 5.6) - Page number not visible in image