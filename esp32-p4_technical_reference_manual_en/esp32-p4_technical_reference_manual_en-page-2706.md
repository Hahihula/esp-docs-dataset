
```markdown
## 53.5 Interrupts

ESP32-P4's TWAI can generate the following interrupt signal that will be sent to the **Interrupt Matrix**.
*   TWAI_INT

There are several internal interrupt sources from the TWAI that can generate the above interrupt signal. The interrupt sources from the TWAI are listed with their trigger conditions and the resulted interrupt signal in Table 53.5-1.

Table 53.5-1. TWAI's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                                                                                                                                                                                                                       | Interrupt Signal |
|:--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------|
| **TWAI_RECEIVE_INT (RXI)** | The Receive Interrupt (RXI) is asserted whenever the TWAI controller has received messages that are pending to be read from the Receive Buffer (i.e., when `TWAI_RX_MESSAGE_COUNTER_REG > 0`). Pending received messages includes valid messages in the Receive FIFO and also overrun messages. The RXI will not be deasserted until all pending received messages are cleared using the **TWAI_RELEASE_BUFFER** command bit. | TWAI_INT         |
| **TWAI_TRANSMIT_INT (TXI)** | The Transmit Interrupt (TXI) is triggered whenever Transmit Buffer becomes free, indicating another message can be loaded into the Transmit Buffer for transmission. The Transmit Buffer becomes free under the following scenarios:<ul><li>A message transmission has completed successfully, i.e., acknowledged without any errors. Any failed messages will automatically be resent.</li><li>A single shot transmission has completed (successfully or unsuccessfully, indicated by the `TWAI_STATUS_TRANSMISSION_COMPLETE` bit).</li><li>A message transmission was aborted using the `TWAI_ABORT_TX` command bit.</li></ul> | TWAI_INT         |

Cont'd on next page
```