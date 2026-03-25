

```markdown
Chapter 27 I2C Controller (I2C)

GoBack

Chapter 27

I2C Controller (I2C)

The I2C (Inter-Integrated Circuit) bus allows ESP32-C61 to communicate with multiple external devices. These external devices can share one I2C bus.

ESP32-C61 has one I2C controller in the main system. It can act as a master or a slave (referred to as I2C below).

27.1 Overview

The I2C bus has two lines, namely a serial data line (SDA) and a serial clock line (SCL). Both SDA and SCL lines are open-drain. The I2C bus can be connected to a single or multiple master devices and a single or multiple slave devices. However, only one master device can access a slave at a time via the bus.

In I2C communication, the master device controls data transmission by sending signals. Key steps include initiating communication with a start signal, transmitting the address and read/write bit, receiving an acknowledge signal, transferring data, and terminating or restarting the communication.

*   Start signal The master initiates communication by generating a START condition: pulling the SDA line low while SCL is high
*   Address and read/write bits Then it issues nine clock pulses via SCL. The first eight pulses are used to transmit a 7-bit address followed by a read/write (R/W) bit.
*   Slave acknowledge If the address of an I2C slave matches the 7-bit address transmitted, this matching slave can respond by pulling SDA low on the ninth clock pulse.
*   Data Transmission The master and the slave can send or receive data according to the R/W bit. Whether to terminate the data transfer or not is determined by the logic level of the acknowledge (ACK) bit. During data transfer, SDA changes only when SCL is low.
*   Termination signal Once the communication has finished, the master sends a STOP condition: pulling SDA up while SCL is high.
*   RSTART signal If a master both reads and writes data in one transfer, then it should send a RSTART condition, a slave address, and a R/W bit before changing its operation. The RSTART condition is used to change the transfer direction and the mode of the devices (master mode or slave mode).

27.2 Feature List

The I2C controller of ESP32-C61 has the following features:

*   Master mode and slave mode
*   Communication between multiple masters and slaves
```