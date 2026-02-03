**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Section Number and Name:**
24. I2C\_\_master executes the STOP command to stop transfer, and generates an I2C\_TRANS\_COMPLETE\_INT (master) interrupt.

**Subheading:**
27.6 Interrupts

**Body Text with List of Interrupts:**

- **I2C\_SLAVE\_STRETCH\_INT:** Generated when one of the four stretching events occurs in slave mode.
  
- **I2C\_DET\_START\_INT:** Triggered when the master or the slave detects a START bit.

- **I2C\_SCL\_MAIN\_ST\_TO\_INT:** Triggered when the main state machine SCL\_MAIN\_FSM remains unchanged for over I2C\_SCL\_MAIN\_ST\_TO\_I2C[23:0] clock cycles.
  
- **I2C\_SCL\_ST\_TO\_INT:** Triggered when the state machine SCL\_FSM remains unchanged for over I2C\_SCL\_ST\_TO\_I2C[23:0] clock cycles.

- **I2C\_RXFIFO\_UDF\_INT:** Triggered when the I2C controller reads RX FIFO via the APB bus, but RX FIFO is empty.
  
- **I2C\_TXFIFO\_OVF\_INT:** Triggered when the I2C controller writes TX FIFO via the APB bus, but TX FIFO is full.

- **I2C\_NACK\_INT:** Triggered when the ACK value received by the master is not as expected, or when the ACK value received by the slave is 1.
  
- **I2C\_TRANS\_START\_INT:** Triggered when the I2C controller sends a START bit.

- **I2C\_TIME\_OUT\_INT:** Triggered when SCL stays high or low for more than \(2^{I2C\_TIME_OUT\_VALUE}\) clock cycles during data transfer.
  
- **I2C\_TRANS\_COMPLETE\_INT:** Triggered when the I2C controller detects a STOP bit.

- **I2C\_MST\_TXFIFO\_UDF\_INT:** Triggered when TX FIFO of the master underflows.
  
- **I2C\_ARBITRATION\_LOST\_INT:** Triggered when the SDA’s output value does not match its input value while the master’s SCL is high.

- **I2C\_BYTE\_TRANS\_DONE\_INT:** Triggered when the I2C controller sends or receives a byte.
  
- **I2C\_END\_DETECT\_INT:** Triggered when op\_code of the master indicates an END command and an END condition is detected.
  
- **I2C\_RXFIFO\_OVF\_INT:** Triggered when RX FIFO of the I2C controller overflows.

- **I2C\_TXFIFO\_WM\_INT:** I2C TX FIFO watermark interrupt. Triggered when I2C\_FIFO\_PRT\_EN is 1 and the pointers of TX FIFO are less than I2C\_TXFIFO\_WM\_THRHD[4:0].
  
- **I2C\_RXFIFO\_WM\_INT:** I2C RX FIFO watermark interrupt. Triggered when I2C\_FIFO\_PRT\_EN is 1 and the pointers of RX FIFO are greater than I2C\_RXFIFO\_WM\_THRHD[4:0].

**Footer Information:**
Espressif Systems
Page number (center-aligned): 1015
Document version information at bottom right corner:
ESP32-S3 TRM (Version 1.7)
Link to submit documentation feedback