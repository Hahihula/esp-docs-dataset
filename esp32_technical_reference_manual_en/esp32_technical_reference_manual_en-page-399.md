**Title:**
Chapter 21 I2C Controller (I2C)

**Diagram Description:**
- The diagram is labeled "Figure 21.3-12 Master Reads from Slave with 7-bit Address in Three Segments".
- It shows the communication between a master and slave over an I2C bus, divided into three segments.
- Each segment includes fields for command (cmd), operation code (op_code), register number (byte_num), address (addr), RAM data read (read) or write status.

**Subtitle:**
21.3.7 Interrupts

**List of Interrupts with Descriptions:**
- I2C_TX_SEND_EMPTY_INT: Triggered when the Master or Slave has sent nonfifo_tx_thres bytes of data.
- I2C_RX_REC_FULL_INT: Triggered when the Master or Slave has received nonfifo_rx_thres bytes of data.
- I2C_ACK_ERR_INT: Triggered when the Master receives an ACK that is not as expected, or when the Slave receives an ACK which value is 1.
- I2CTrans_START_INT: Triggered when the Master or Slave sends the START bit.
- I2C_TIME_OUT_INT: Triggered when the SCL stays high or low for more than I2C_TIME_OUT clocks.
- I2CTrans_COMPLETE_INT: Triggered when the Master or Slave detects a STOP bit.
- I2C_MASTER_TRAN COMP_INT: Triggered when the Master sends or receives a byte.
- I2C_ARBITRATION_LOST_INT: Triggered when the Master’s SCL is high, while the output value and input value of the SDA do not match.
- I2C_SLAVE_TRANComp_INT: Triggered when the Slave sends or receives a byte.
- I2C_END_DETECT_INT: Triggered when the Master deals with the END command.
- I2C_RXFIFO_OVF_INT: Triggered when RX FIFO of the I2C controller overflows.

**Footer Information:**
- Espresso Systems
- Page number 399
- Document version ESP32 TRM (Version 5.6)
- Submit Documentation Feedback