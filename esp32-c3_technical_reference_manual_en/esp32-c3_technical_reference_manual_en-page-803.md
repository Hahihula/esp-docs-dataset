

```markdown
could indicate one of the following events, depending on the values TWAI_ERR_ST and TWAI_BUS_OFF_ST at the moment when the EWI is triggered.

* If `TWAI_ERR_ST = 0` and `TWAI_BUS_OFF_ST = 0`:
    - If the TWAI controller was in the Error Active state, it indicates both the TEC and REC have returned below the threshold value set by `TWAI_ERR_WARNING_LIMIT_REG`.
    - If the TWAI controller was previously in the Bus Off Recovery state, it indicates that Bus Recovery has completed successfully.
* If `TWAI_ERR_ST = 1` and `TWAI_BUS_OFF_ST = 0`: The TEC or REC error counters have exceeded the threshold value set by `TWAI_ERR_WARNING_LIMIT_REG`.
* If `TWAI_ERR_ST = 1` and `TWAI_BUS_OFF_ST = 1`: The TWAI controller has entered the BUS_OFF state (due to the TEC >= 256).
* If `TWAI_ERR_ST = 0` and `TWAI_BUS_OFF_ST = 1`: The TWAI controller’s TEC has dropped below the threshold value set by `TWAI_ERR_WARNING_LIMIT_REG` during BUS_OFF recovery.

### 31.4.3.4 Data Overrun Interrupt (DOI)

The Data Overrun Interrupt (DOI) is triggered whenever the Receive FIFO has overrun. The DOI indicates that the Receive FIFO is full and should be cleared immediately to prevent any further overrun messages.

The DOI is only triggered by the first message that causes the Receive FIFO to overrun (i.e., the transition from the Receive FIFO not being full to the Receive FIFO overrunning). Any subsequent overrun messages will not trigger the DOI again. The DOI could be triggered again when all received messages (valid or overrun) have been cleared.

### 31.4.3.5 Error Passive Interrupt (TXI)

The Error Passive Interrupt (EPI) is triggered whenever the TWAI controller switches from Error Active to Error Passive, or vice versa.

### 31.4.3.6 Arbitration Lost Interrupt (ALI)

The Arbitration Lost Interrupt (ALI) is triggered whenever the TWAI controller is attempting to transmit a message and loses arbitration. The bit position where the TWAI controller lost arbitration is automatically recorded in Arbitration Lost Capture register (`TWAI_ARB_LOST_CAP_REG`). When the ALI occurs again, the Arbitration Lost Capture register will no longer record new bit location until it is cleared (via CPU reading this register).

### 31.4.3.7 Bus Error Interrupt (BEI)

The Bus Error Interrupt (BEI) is triggered whenever TWAI controller detects an error on the TWAI bus. When a bus error occurs, the Bus Error type and its bit position are automatically recorded in the Error Code Capture register (`TWAI_ERR_CODE_CAP_REG`). When the BEI occurs again, the Error Code Capture register will no longer record new error information until it is cleared (via a read from the CPU).
```