

```markdown
29.7 Interrupts

*   I2C_SLAVE_STRETCH_INT: Generated when one of the four stretching events occurs in slave mode.
*   I2C_DET_START_INT: Triggered when the master or the slave detects a START signal.
*   I2C_SCL_MAIN_ST_TO_INT: Triggered when the main state machine SCL_MAIN_FSM remains unchanged for over `I2C_SCL_MAIN_ST_TO_I2C[23:0]` clock cycles.
*   I2C_SCL_ST_TO_INT: Triggered when the state machine SCL FSM remains unchanged for over `I2C_SCL_ST_TO_I2C[23:0]` clock cycles.
*   I2C_RXFIFO_UDF_INT: Triggered when the I2C controller reads RX FIFO via the APB bus, but RX FIFO is empty.
*   I2C_TXFIFO_OVF_INT: Triggered when the I2C controller writes TX FIFO via the APB bus, but TX FIFO is full.
*   I2C_NACK_INT: Triggered when the ACK value received by the master is not as expected, or when the ACK value received by the slave is 1.
*   I2C_TRANS_START_INT: Triggered when the I2C controller sends a START bit.
*   I2C_TIME_OUT_INT: Triggered when SCL stays high or low for more than `2^I2C_TIME_OUT_VALUE` clock cycles during data transfer.
*   I2C_TRANS_COMPLETE_INT: Triggered when the I2C controller detects a STOP bit.
*   I2C_MST_TXFIFO_UDF_INT: Triggered when TX FIFO of the master underflows.
*   I2C_ARBITRATION_LOST_INT: Triggered when the SDA’s output value does not match its input value while the master’s SCL is high.
*   I2C_BYTE_TRANS_DONE_INT: Triggered when the I2C controller sends or receives a byte.
*   I2C_END_DETECT_INT: Triggered when `op_code` of the master indicates an END command and an END condition is detected.
*   I2C_RXFIFO_OVF_INT: Triggered when RX FIFO of the I2C controller overflows.
*   I2C_TXFIFO_WM_INT: I2C TX FIFO watermark interrupt. Triggered when `I2C_FIFO_PRT_EN` is 1 and the pointers of TX FIFO are less than `I2C_TXFIFO_WM_THRHD[4:0]`.
*   I2C_RXFIFO_WM_INT: I2C RX FIFO watermark interrupt. Triggered when `I2C_FIFO_PRT_EN` is 1 and the pointers of RX FIFO are greater than `I2C_RXFIFO_WM_THRHD[4:0]`.
*   I2C_SLAVE_ADDR_UNMATCH_INT: Triggered when the received slave address is inconsistent with the internally configured slave address in slave mode.
```