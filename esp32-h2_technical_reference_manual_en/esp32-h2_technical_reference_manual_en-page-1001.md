
```markdown
Chapter 34 Two-wire Automotive Interface (TWAI)

GoBack

34.4.3.1 Receive Interrupt (RXI)

The Receive Interrupt (RXI) is asserted whenever the TWAI controller has received messages that are pending to be read from the Receive Buffer (i.e., when `TWAI_RX_MESSAGE_CNT_REG > 0`). Pending received messages includes valid messages in the Receive FIFO and also overrun messages. The RXI will not be deasserted until all pending received messages are cleared using the `TWAI_RELEASE_BUF` command bit.

34.4.3.2 Transmit Interrupt (TXI)

The Transmit Interrupt (TXI) is triggered whenever Transmit Buffer becomes free, indicating another message can be loaded into the Transmit Buffer to be transmitted. The Transmit Buffer becomes free under the following scenarios:

- A message transmission has been completed successfully, i.e., acknowledged without any errors. Any failed messages will automatically be resent.
- A single shot transmission has been completed (successfully or unsuccessfully, indicated by the `TWAI_TX_COMPLETE` bit).
- A message transmission was aborted using the `TWAI_ABORT_TX` command bit.

34.4.3.3 Error Warning Interrupt (EWI)

The Error Warning Interrupt (EWI) is triggered whenever there is a change to the `TWAI_ERR_ST` and `TWAI_BUS_OFF_ST` bits of `TWAI_STATUS_REG` (i.e., transition from 0 to 1 or vice versa). Thus, an EWI could indicate one of the following events, depending on the values of `TWAI_ERR_ST` and `TWAI_BUS_OFF_ST` at the moment when the EWI is triggered.

- If `TWAI_ERR_ST = 0` and `TWAI_BUS_OFF_ST = 0`:
    - If the TWAI controller was in the Error Active state, it indicates both the TEC and REC have returned below the threshold value set by `TWAI_ERR_WARNING_LIMIT_REG`.
    - If the TWAI controller was previously in the Bus Off Recovery state, it indicates that Bus Recovery has completed successfully.
- If `TWAI_ERR_ST = 1` and `TWAI_BUS_OFF_ST = 0`: The TEC or REC error counters have exceeded the threshold value set by `TWAI_ERR_WARNING_LIMIT_REG`.
- If `TWAI_ERR_ST = 1` and `TWAI_BUS_OFF_ST = 1`: The TWAI controller has entered the BUS_OFF state (due to the TEC >= 256).
- If `TWAI_ERR_ST = 0` and `TWAI_BUS_OFF_ST = 1`: The TWAI controller’s TEC has dropped below the threshold value set by `TWAI_ERR_WARNING_LIMIT_REG` during BUS_OFF recovery.

34.4.3.4 Data Overrun Interrupt (DOI)

The Data Overrun Interrupt (DOI) is triggered whenever the Receive FIFO has overrun. The DOI indicates that the Receive FIFO is full and should be cleared immediately to prevent any further overrun messages.

The DOI is only triggered by the first message that causes the Receive FIFO to overrun (i.e., the transition from the Receive FIFO not being full to the Receive FIFO overrunning). Any subsequent overrun messages will not
```