

# Chapter 30

## I2C Controller (I2C)

The I2C (Inter-Integrated Circuit) bus allows ESP32-H2 to communicate with multiple external devices. These external devices can share one I2C bus. ESP32-H2 has two I2C controllers in the main system, which can act as a master or a slave.

### 30.1 Overview

The I2C bus has two lines, namely a serial data line (SDA) and a serial clock line (SCL). Both SDA and SCL lines are open-drain. Therefore, multiple peripherals can be mounted on the I2C bus, usually with one or more masters and one or more slaves. However, only one master is allowed to occupy the bus to access one slave at the same time.

The master initiates communication by generating a START condition: pulling the SDA line low while SCL is high. Then it issues nine clock pulses via SCL. The first eight pulses are used to transmit a 7-bit address followed by a read/write (R/W) bit. If the address of an I2C slave matches the 7-bit address transmitted, this matching slave can respond by pulling SDA low on the ninth clock pulse. Then, the master and the slave can send or receive data according to the R/W bit, and terminate the data transfer according to the logic level of the acknowledge (ACK) bit. During data transfer, SDA changes only when SCL is low. Once the communication has finished, the master sends a STOP condition: pulling SDA up while SCL is high. If a master both reads and writes data in one transfer, then it should send an RSTART condition, a slave address, and a R/W bit before switching between the operations. The RSTART condition is used to change the transfer direction and the mode of the devices (master mode or slave mode).

### 30.2 Features

The I2C controller of ESP32-H2 has the following features:

* Master mode and slave mode
* Communication between multiple masters and slaves
* Standard mode (100 Kbit/s)
* Fast mode (400 Kbit/s)
* 7-bit addressing and 10-bit addressing
* Continuous data transfer by pulling SCL low in slave mode
* Programmable digital noise filtering
* Dual address mode, which uses slave address and slave memory or register address