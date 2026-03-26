

```markdown
| Bit 31-8 | Bit 7   | Bit 6    | Bit 5     | Bit 4   | Bit 3   | Bit 2   | Bit 1   | Bit 0 |
|----------|---------|----------|-----------|---------|---------|---------|---------|-------|
| Reserved | SAM     | PBS2.2   | PBS2.1    | PBS2.0  | PBS1.3  | PBS1.2  | PBS1.1  | PBS1.0|

Notes:
* PBS1: The number of Time Quanta in Phase Buffer Segment 1 is defined based on PBS1 + 1.
* PBS2: The number of Time Quanta in Phase Buffer Segment 2 is defined based on PBS2 + 1.
* SAM: Enables triple sampling if set to 1. This is useful for low/medium speed buses to filter spikes on the bus line.

## 53.4.3 Transmit and Receive Buffers

### 53.4.3.1 Overview of Buffers

Table 53.4-3. Buffer Layout for Standard Frame Format and Extended Frame Format

| Standard Frame Format (SFF) |          | Extended Frame Format (EFF) |          |
|-----------------------------|----------|----------------------------|----------|
| Offset Address              | Content  | Offset Address             | Content  |
| 0x40                        | TX/RX frame information | 0x40                     | TX/RX frame information |
| 0x44                        | TX/RX identifier 1       | 0x44                     | TX/RX identifier 1      |
| 0x48                        | TX/RX identifier 2       | 0x48                     | TX/RX identifier 2      |
| 0x4c                        | TX/RX data byte 1        | 0x4c                     | TX/RX identifier 3      |
| 0x50                        | TX/RX data byte 2        | 0x50                     | TX/RX identifier 4      |
| 0x54                        | TX/RX data byte 3        | 0x54                     | TX/RX data byte 1       |
| 0x58                        | TX/RX data byte 4        | 0x58                     | TX/RX data byte 2       |
| 0x5c                        | TX/RX data byte 5        | 0x5c                     | TX/RX data byte 3       |
| 0x60                        | TX/RX data byte 6        | 0x60                     | TX/RX data byte 4       |
| 0x64                        | TX/RX data byte 7        | 0x64                     | TX/RX data byte 5       |
| 0x68                        | TX/RX data byte 8        | 0x68                     | TX/RX data byte 6       |
| 0x6c                        | reserved                 | 0x6c                     | TX/RX data byte 7       |
| 0x70                        | reserved                 | 0x70                     | TX/RX data byte 8       |

Table 53.4-3 illustrates the layout of the Transmit Buffer and Receive Buffer registers. Both the Transmit and Receive Buffer registers share the same address space and are only accessible when the TWAI controller is in Operation mode. The CPU accesses Transmit Buffer registers for write operations, and Receive Buffer registers for read operations. Both buffers share the exact same register layout and fields to store a message (received or to be transmitted). The Transmit Buffer registers are used to configure a TWAI message to be transmitted. The CPU would write to the Transmit Buffer registers specifying the message's frame type, frame format, frame ID, and frame data (payload). Once the Transmit Buffer is configured, the CPU would then initiate the transmission by setting the `TWAI_TX_REQUEST` bit in `TWAI_CMD_REG`.

* For a self-reception request, set the `TWAI_SELF_RX_REQUEST` bit instead.
* For a single-shot transmission, set both the `TWAI_TX_REQUEST` and the `TWAI_ABORT_TX` simultaneously.
```