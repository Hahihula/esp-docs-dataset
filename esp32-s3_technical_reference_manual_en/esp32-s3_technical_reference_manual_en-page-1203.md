Title: Chapter 31 Two-wire Automotive Interface (TWAI®)

Subtitle: GoBack

Section Title:
- **31.5.3.7 Bus Error Interrupt (BEI)**

Body Text:
The Bus Error Interrupt (BEI) is triggered whenever TWAI controller detects an error on the TWAI bus. When a bus error occurs, the Bus Error type and its bit position are automatically recorded in the Error Code Capture register (`TWAI_ERR_CODE_CAP_REG`). When the BEI occurs again, the Error Code Capture register will no longer record new error information until it is cleared (via a read from the CPU).

Section Title:
- **31.5.3.8 Bus Status Interrupt (BSI)**

Body Text:
The Bus Status Interrupt (BSI) is triggered whenever TWAI controller is switching between receive/transmit status and idle status. When a BSI occurs, the current status of TWAI controller can be measured by reading `TWAI_RX_ST` and `TWAI_TX_ST` in `TWAI_STATUS_REG` register.

Section Title:
- **31.5.4 Transmit and Receive Buffers**

Subsection Title: 
- **31.5.4.1 Overview of Buffers**

Table Caption (with table):
- Table 31.5-3. Buffer Layout for Standard Frame Format and Extended Frame Format

Table Content:

| TWAI Address | Contenent       | TWAI Address | Content                   |
|--------------|-----------------|--------------|---------------------------|
| 0x40         | TX/RX frame information | 0x40        | TX/RX frame information   |
| 0x44         | TX/RX identifier 1    | 0x44        | TX/RX identifier 1       |
| 0x48         | TX/RX identifier 2    | 0x48        | TX/RX identifier 2       |
| 0x4c         | TX/RX data byte 1     | 0x4c        | TX/RX identifier 3       |
| 0x50         | TX/RX data byte 2     | 0x50        | TX/RX identifier 4       |
| 0x54         | TX/RX data byte 3     | 0x54        | TX/RX data byte 1        |
| 0x58         | TX/RX data byte 4     | 0x58        | TX/RX data byte 2        |
| 0x5c         | TX/RX data byte 5     | 0x5c        | TX/RX data byte 3        |
| 0x60         | TX/RX data byte 6     | 0x60        | TX/RX data byte 4        |
| 0x64         | TX/RX data byte 7     | 0x64        | TX/RX data byte 5        |
| 0x68         | TX/RX data byte 8     | 0x68        | TX/RX data byte 6        |
| **0x6c**    | reserved          | **0x70**    | reserved                  |

Body Text:
Table 31.5-3 illustrates the layout of the Transmit Buffer and Receive Buffer registers. Both the Transmit and Receive Buffer registers share the same address space and are only accessible when the TWAI controller is in Operation Mode. CPU write operations access the Transmit Buffer registers, and CPU read operations access the Receive Buffer registers. However, both buffers share the exact same register layout and fields to represent a message (received or to be transmitted). The Transmit Buffer registers are used to configure a TWAI message to be transmitted. The CPU would write to the Transmit Buffer registers specifying the message's frame type, frame format, frame ID, and frame data (payload). Once the Transmit Buffer is configured, the CPU would then initiate the transmission by setting the `TWAI_TX_REQ` bit in `TWAI_CMD_REG`.

- For a self-reception request, set the `TWAI SELF_RX_REQ` bit instead.
- For a single-shot transmission, set both the `TWAI_TX_REQ` and the `TWAI_ABORT_TX` simultaneously.

Footer:
Espressif Systems
1203 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback