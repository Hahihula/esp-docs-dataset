

# Chapter 44

## I2C Controller (I2C)

The I2C (Inter-Integrated Circuit) bus allows ESP32-P4 to communicate with multiple external devices. These external devices can share one I2C bus. ESP32-P4 has three I2C controllers: two in the main system and one in the low-power system. The two I2C controllers in the main system can act as a master or a slave (referred to as I2C below), while the one in the low-power system can only act as a master (referred to as LP_I2C below), which can still work when the main system sleeps.

### 44.1 Overview

The I2C bus has two lines, namely a serial data line (SDA) and a serial clock line (SCL). Both SDA and SCL lines are open-drain. The I2C bus can be connected to a single or multiple master devices and a single or multiple slave devices. However, only one master device can access a slave at a time via the bus.

The master initiates communication by generating a START condition: pulling the SDA line low while SCL is high. Then it issues nine clock pulses via SCL. The first eight pulses are used to transmit a 7-bit address followed by a read/write (R/W) bit. If the address of an I2C slave matches the 7-bit address transmitted, this matching slave can respond by pulling SDA low on the ninth clock pulse. The master and the slave can send or receive data according to the R/W bit. Whether to terminate the data transfer or not is determined by the logic level of the acknowledge (ACK) bit. During data transfer, SDA changes only when SCL is low. Once the communication has finished, the master sends a STOP condition: pulling SDA up while SCL is high. If a master both reads and writes data in one transfer, then it should send a RSTART condition, a slave address, and a R/W bit before changing its operation. The RSTART condition is used to change the transfer direction and the mode of the devices (master mode or slave mode).

### 44.2 Features

The I2C controller of ESP32-P4 has the following features:

* Master mode and slave mode
* Communication between multiple masters and slaves
* Standard mode (100 Kbit/s)
* Fast mode (400 Kbit/s)
* 7-bit addressing and 10-bit addressing
* Continuous data transfer achieved by pulling SCL low in slave mode
* Programmable digital noise filtering
* Dual address mode, which uses slave address and slave memory or register address