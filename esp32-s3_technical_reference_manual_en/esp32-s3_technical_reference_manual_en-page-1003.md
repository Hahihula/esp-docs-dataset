Title: Chapter 27 I2C Controller (I2C)

Body Text:
ready and `I2CTransStart` is set, `I2Cmaster` initiates data transfer. After executing the END command,
`I2Cmaster` turns off the SCL clock and pulls SCL low to reserve the bus. Meanwhile, the controller generates an
`I2C_endDetectInt` interrupt.

For the second segment, after detecting the I2C_END_DETECT_INT interrupt, software refreshes the
CMD_Controller registers, reloads the RAM and clears this interrupt, as shown in Segment1. If `cmd1` in the
second segment is a STOP, then data is transmitted to `I2Cslave` in two segments. `I2Cmaster` resumes data
transfer after `I2C_transStart` set, and terminates the transfer by sending a STOP bit.

For the third segment, after the second data transfer finishes and an I2C_END_DETECT_INT is detected,
the CMD_Controller registers of `I2Cmaster` are configured as shown in Segment2. Once `I2C_transStart` is set,
`I2Cmaster` generates a STOP bit and terminates the transfer.

Note that other `I2Cmasters` will not transact on the bus between two segments. The bus is only released after a
STOP signal is sent. The I2C controller can be reset by setting `I2C_fsmRst` field at any time. This field will
later be cleared automatically by hardware.

Subtitle: 27.5.4.2 Configuration Example

List:
1. Set `I2C_msMode` (master) to 1, and `I2C_msMode` (slave) to 0.
2. Write 1 to `I2C_confUpdate` (master) and `I2C_confUpdate` (slave) to synchronize registers.
3. Configure command registers of `I2Cmaster`.

Table:
- Command registers
  - `I2C_COMMAND0` (master): RSTART, ack_value: —, ack_exp: —, ack_check_en: —, byte_num: —
  - `I2C_COMMAND1` (master): WRITE, ack_value: —, ack_exp: N+1, ack_check_en: I2C_NACK_INT, byte_num: —
  - `I2C_COMMAND2` (master): END, ack_value: —, ack_exp: —, ack_check_en: —, byte_num: —

4. Write the address of `I2Cslave` and data to be sent to TX RAM of `I2Cmaster` in either FIFO mode or non-FIFO
   mode according to Section 27.4.10.
5. Write the address of `I2Cslave` to `I2C_slaveAddr` (slave) in `I2C_slaveAddrReg` (slave) register
6. Write 1 to `I2C_confUpdate` (master) and `I2C_confUpdate` (slave) to synchronize registers.
7. Write 1 to `I2C_transStart` (master) and `I2C_transStart` (slave) to start transfer.

8. `I2Cslave` compares the slave address sent by `I2Cmaster` with its own address in `I2C_slaveAddr`
   When ack_check_en (master) in `I2Cmaster`'s WRITE command is 1, `I2Cmaster` checks ACK value each time it
   sends a byte. When ack_check_en (master) is 0, `I2Cmaster` does not check ACK value and take `I2Cslave`
   as matching slave by default.
   - Match: If the received ACK value matches ack_exp (master) (the expected ACK value), `I2Cmaster`
     continues data transfer.
   - Not match: If the received ACK value does not match ack_exp, `I2Cmaster` generates an
     `I2C_NACK_INT` (master) interrupt and stops data transfer.

9. `I2Cmaster` sends data, and checks ACK value or not according to ack_check_en (master).

Footer:
Espressif Systems

Page Number: 1003

Document Title: ESP32-S3 TRM (Version 1.7)

Link Text: Submit Documentation Feedback