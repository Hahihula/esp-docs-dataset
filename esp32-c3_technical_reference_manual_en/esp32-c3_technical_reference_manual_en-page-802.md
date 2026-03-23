
```markdown
## 31.4.3 Interrupt Management

The ESP32-C3 TWAI controller provides eight interrupts, each represented by a single bit in the `TWAI_INT_RAW_REG`. For a particular interrupt to be triggered, the corresponding enable bit in `TWAI_INT_ENA_REG` must be set.

The TWAI controller provides the following interrupts:

* Receive Interrupt
* Transmit Interrupt
* Error Warning Interrupt
* Data Overrun Interrupt
* Error Passive Interrupt
* Arbitration Lost Interrupt
* Bus Error Interrupt
* Bus Status Interrupt

The TWAI controller's interrupt signal to the interrupt matrix will be asserted whenever one or more interrupt bits are set in the `TWAI_INT_RAW_REG`, and deasserted when all bits in `TWAI_INT_RAW_REG` are cleared. The majority of interrupt bits in `TWAI_INT_RAW_REG` are automatically cleared when the register is read, except for the Receive Interrupt which can only be cleared when all the messages are released by setting the `TWAI_RELEASE_BUF` bit.

### 31.4.3.1 Receive Interrupt (RXI)

The Receive Interrupt (RXI) is asserted whenever the TWAI controller has received messages that are pending to be read from the Receive Buffer (i.e., when `TWAI_RX_MESSAGE_CNT_REG > 0`). Pending received messages includes valid messages in the Receive FIFO and also overrun messages. The RXI will not be deasserted until all pending received messages are cleared using the `TWAI_RELEASE_BUF` command bit.

### 31.4.3.2 Transmit Interrupt (TXI)

The Transmit Interrupt (TXI) is triggered whenever Transmit Buffer becomes free, indicating another message can be loaded into the Transmit Buffer to be transmitted. The Transmit Buffer becomes free under the following scenarios:

* A message transmission has completed successfully, i.e., acknowledged without any errors. (Any failed messages will automatically be resent.)
* A single shot transmission has completed (successfully or unsuccessfully, indicated by the `TWAI_TX_COMPLETE` bit).
* A message transmission was aborted using the `TWAI_ABORT_TX` command bit.

### 31.4.3.3 Error Warning Interrupt (EWI)

The Error Warning Interrupt (EWI) is triggered whenever there is a change to the `TWAI_ERR_ST` and `TWAI_BUS_OFF_ST` bits of the `TWAI_STATUS_REG` (i.e., transition from 0 to 1 or vice versa). Thus, an EWI
```