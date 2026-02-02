**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Body Text:**

The TWAI controller provides seven following interrupts:

- Receive Interrupt
- Transmit Interrupt
- Error Warning Interrupt
- Data Overrun Interrupt
- Error Passive Interrupt
- Arbitration Lost Interrupt
- Bus Error Interrupt

The TWAI controller’s interrupt signal to the interrupt matrix will be asserted whenever one or more interrupt bits are set in the `TWAI_INT_RAW_REG`, and deasserted when all bits in `TWAI_INT_RAW_REG` are cleared. The majority of interrupt bits in `TWAI_INT_RAW_REG` are automatically cleared when the register is read. However, the Receive Interrupt is an exception and can only be cleared the Receive FIFO is empty.

**Subtitle: 25.5.3.1 Receive Interrupt (RXI)**

The Receive Interrupt (RXI) is asserted whenever the TWAI controller has received messages that are pending to read from the Receive Buffer (i.e., when `TWAI_RX_MESSAGE_CNT_REG` > 0). Pending received messages includes valid messages in the Receive FIFO and also overrun messages. The RXI will not be deasserted until all pending received messages are cleared using the `TWAI_RELEASE_BUF` command bit.

**Subtitle: 25.5.3.2 Transmit Interrupt (TXI)**

The Transmit Interrupt (TXI) is triggered whenever Transmit Buffer becomes free, indicating another message can be loaded into the Transmit Buffer to be transmitted. The Transmit Buffer becomes free under the following scenarios:

- A message transmission has completed successfully (i.e., Acknowledged without any errors). Any failed messages will automatically be retried.
- A single shot transmission has completed (successfully or unsuccessfully, indicated by the `TWAI_TX_COMPLETE` bit).
- A message transmission was aborted using the `TWAI_ABORT_TX` command and bit.

**Subtitle: 25.5.3.3 Error Warning Interrupt (EWI)**

The Error Warning Interrupt (EWI) is triggered whenever there is a change to the `TWAI_ERR_ST` and `TWAI_BUS_OFF_ST` bits of the `TWAI_STATUS_REG` (i.e., transition from 0 to 1 or vice versa). Thus, an EWI could indicate one of the following events, depending on the values `TWAI_ERR_ST` and `TWAI_BUS_OFF_ST` at the moment the EWI is triggered.

- If `TWAI_ERR_ST = 0` and `TWAI_BUS_OFF_ST = 0`:
  - If the TWAI controller was in the Error Active state, it indicates both the TEC and REC have returned below the threshold value set by `TWAI_ERR_WARNING_LIMIT_REG`.
  - If the TWAI controller was previously in the Bus Recovery state, it indicates that Bus Recovery has completed successfully.

**Footer:**
Espressif Systems
539 ESP32 TRM (Version 5.6)