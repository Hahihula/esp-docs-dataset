

```markdown
| Standard Frame Format (SFF) | Extended Frame Format (EFF) |
|------------------------------|-----------------------------|
| TWAI Address                 | Content                     | TWAI Address | Content                      |
| 0x40                         | TX/RX frame information     | 0x40         | TX/RX frame information       |
| 0x44                         | TX/RX identifier 1          | 0x44         | TX/RX identifier 1            |
| 0x48                         | TX/RX identifier 2          | 0x48         | TX/RX identifier 2            |
| 0x4c                         | TX/RX data byte 1           | 0x4c         | TX/RX identifier 3            |
| 0x50                         | TX/RX data byte 2           | 0x50         | TX/RX identifier 4            |
| 0x54                         | TX/RX data byte 3           | 0x54         | TX/RX data byte 1             |
| 0x58                         | TX/RX data byte 4           | 0x58         | TX/RX data byte 2             |
| 0x5c                         | TX/RX data byte 5           | 0x5c         | TX/RX data byte 3             |
| 0x60                         | TX/RX data byte 6           | 0x60         | TX/RX data byte 4             |
| 0x64                         | TX/RX data byte 7           | 0x64         | TX/RX data byte 5             |
| 0x68                         | TX/RX data byte 8           | 0x68         | TX/RX data byte 6             |
| 0x6c                         | reserved                    | 0x6c         | TX/RX data byte 7             |
| 0x70                         | reserved                    | 0x70         | TX/RX data byte 8             |
```

Table 31.4-3 illustrates the layout of the Transmit Buffer and Receive Buffer registers. Both the Transmit and Receive Buffer registers share the same address space and are only accessible when the TWAI controller is in Operation Mode. The CPU accesses Transmit Buffer registers for write operations, and Receive Buffer registers for read operations. Both buffers share the exact same register layout and fields to represent a message (received or to be transmitted). The Transmit Buffer registers are used to configure a TWAI message to be transmitted. The CPU would write to the Transmit Buffer registers specifying the message's frame type, frame format, frame ID, and frame data (payload). Once the Transmit Buffer is configured, the CPU would then initiate the transmission by setting the `TWAI_TX_REQ` bit in `TWAI_CMD_REG`.

*   For a self-reception request, set the `TWAI_SELF_RX_REQ` bit instead.
*   For a single-shot transmission, set both the `TWAI_TX_REQ` and the `TWAI_ABORT_TX` simultaneously.

The Receive Buffer registers map the first message in the Receive FIFO. The CPU would read the Receive Buffer registers to obtain the first message's frame type, frame format, frame ID, and frame data (payload). Once the message has been read from the Receive Buffer registers, the CPU can set the `TWAI_RELEASE_BUF` bit in `TWAI_CMD_REG` to clear the Receive Buffer registers. If there are still messages in the Receive FIFO, the Receive Buffer registers will map the first message again.
```