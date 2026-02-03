**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Titles and Content:**

- **PBS1:** The number of Time Quanta in Phase Buffer Segment 1 is defined according to the following equation:
  \[
  (\text{8} \times \text{PBS1.3} + 4 \times \text{PBS1.2} + 2 \times \text{PBS1.1} + \text{PBS1.0} + 1)
  \]

- **PBS2:** The number of Time Quanta in Phase Buffer Segment 2 is defined according to the following equation:
  \[
  (\text{4} \times \text{PBS2.2} + 2 \times \text{PBS2.1} + \text{PBS2.0} + 1)
  \]

- **SAM:** Enables triple sampling if set to 1. This is useful for low/medium speed buses to filter spikes on the bus line.

**Subtitle:**
31.5.3 Interrupt Management

**Body Text:**
The ESP32-S3 TWAI controller provides eight interrupts, each represented by a single bit in the `TWAI_INT_RAW_REG`. For a particular interrupt to be triggered, the corresponding enable bit in `TWAI_INT_ENA_REG` must be set.

The TWAI controller provides the following interrupts:
- Receive Interrupt
- Transmit Interrupt
- Error Warning Interrupt
- Data Overrun Interrupt
- Error Passive Interrupt
- Arbitration Lost Interrupt
- Bus Error Interrupt
- Bus Status Interrupt

The TWAI controller’s interrupt signal to the interrupt matrix will be asserted whenever one or more interrupt bits are set in `TWAI_INT_RAW_REG`, and deasserted when all bits in `TWAI_INT_RAW_REG` are cleared. The majority of interrupt bits in `TWAI_INT_RAW_REG` are automatically cleared when the register is read, except for the Receive Interrupt which can only be cleared when all messages are released by setting the `TWAI_RELEASE_BUF` bit.

**Subtitle:**
31.5.3.1 Receive Interrupt (RXI)

**Body Text:**
The Receive Interrupt (RXI) is asserted whenever the TWAI controller has received messages that are pending to be read from the Receive Buffer, i.e., when `TWAI_RX_MESSAGE_CNT_REG > 0`. Pending received messages includes valid messages in the Receive FIFO and also overrun messages. The RXI will not be deasserted until all pending received messages are cleared using the `TWAI_RELEASE_BUF` command bit.

**Subtitle:**
31.5.3.2 Transmit Interrupt (TXI)

**Body Text:**
The Transmit Interrupt (TXI) is triggered whenever Transmit Buffer becomes free, indicating another message can be loaded into the Transmit Buffer to be transmitted. The Transmit Buffer becomes free under the following scenarios:
- A message transmission has completed successfully, i.e., acknowledged without any errors. (Any failed messages will automatically be resent.)

**Footer:**
Espressif Systems
1201 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback