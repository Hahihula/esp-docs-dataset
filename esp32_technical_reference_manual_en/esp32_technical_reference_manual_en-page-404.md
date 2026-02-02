**Chapter:**
21 I²C Controller (I²C)

**Register Information:** 
- **Register Name**: Register 21.3, I²C_SR_REG (0x0008)
- **Address**: Not specified in the text.

**Field Descriptions and Values for I²C SR Register:**

- **I2C_SCL_STATE_LAST**
  - Description: This field indicates the states of the state machine used to produce SCL.
  - Access Type: Read Only (RO).
  - Possible States:
    - Idle
    - Start
    - Negative edge
    - Low
    - Positive edge
    - High
    - Stop

- **I2C_SCL_MAIN_STATE LAST**
  - Description: This field indicates the states of the I²C module state machine.
  - Access Type: Read Only (RO).
  - Possible States:
    - Idle
    - Address shift
    - ACK address
    - Rx data
    - Tx data
    - Send ACK
    - Wait ACK

- **I2C_TXFIFO_CNT**
  - Description: This field stores the amount of received data in RAM.
  - Access Type: Read Only (RO).

- **I2C_RXFIFO_CNT**
  - Description: This field represents the amount of data needed to be sent.
  - Access Type: Read Only (RO).
  
- **I2C_BYTE_TRANS**
  - Description: This field changes to 1 when one byte is transferred.
  - Access Type: Read Only (RO).

- **I2C_SLAVE_ADDRESSED**
  - Description: When configured as an I²C Slave, and the address sent by the master is equal to the address of the slave, then this bit will be at high level. 
  - Access Type: Read Only (RO).
  
- **I2C BUS BUSY**
  - Description: The value indicates whether the bus is busy transferring data.
  - Possible States:
    - I²C bus is idle state
    - I²C bus in idle state
  
- **I2C_ARB_LOST**
  - Description: When this occurs, it means that control of SCL line has been lost by one master or slave. The register changes to a high level.
  - Access Type: Read Only (RO).

- **I2C TIME_OUT**
  - Description: This field indicates the number of I²C_TIME_OUT clocks required for data transfer when an I²C controller takes more than this amount before receiving valid clock cycles from another device. The value changes to a high level.
  - Access Type: Read Only (RO).

- **I2C_SLAVE_RW**
  - Description:
    - When in slave mode, the master reads or writes with respect to data transfer between devices on an I²C bus.

- **I2C_ACK_REC**
  - Description: This register stores the value of received ACK bit.
  - Access Type: Read Only (RO).

**Register Information for Register 21.4:** 
- **Register Name**: Register 21.4, I²C_TO_REG (0x000c)
- **Address**: Not specified in the text.

**Field Description and Values for I²C TO Register:**

- **I2C TIME OUT REG**
  - Description: This register is used to configure the timeout value before receiving a data bit from APB clock cycles.
  - Access Type: Read/Write (R/W).

**Footer Information:** 
- Company Name: Espressif Systems
- Document Version and Title: ESP32 TRM (Version 5.6)
- Page Number: Not specified in the text.

**Navigation Links:**
- Submit Documentation Feedback

(Note: The image contains a diagram with binary values, but it is not described as per your instructions.)