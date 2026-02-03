**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Body Text with List Items and Diagrams:**

- Configures clock parameters
- Configures card command parameters
- Sends commands to card bus (sdhost_ccmd_out line)
- Receives responses from card bus (sdhost_ccmd_in line)
- Sends responses to BIU
- Drives the P-bit on the command line

The command path State Machine is shown in Figure 34.4-2.

**Figure Caption:**
Figure 34.4-2. Command Path State Machine

**Subsection Title and Body Text with Diagrams (continued):**

34.4.3 Data Path
The data path block pops RAM data and transmits them on sdhost_cdata_out during a write-data transfer, or it receives data on sdhost_cdata_in and pushes them into RAM during a read-data transfer. The data path loads new data parameters, i.e., expected data, read/write data transfer, stream/block transfer, block size, byte count, card type, timeout registers, etc., whenever a data transfer command is not in progress.

If the SDHOST_DATAEXPECTED bit is set in SDHOST_CMD_REG register, the new command is a data-transfer command and the data path starts one of the following operations:

- Transmitting data if the SDHOST_READ_WRITE bit is 1
- Receiving data if the SDHOST_READWRITE bit is 0

34.4.3.1 Data Transmit Operation
The module starts data transmission two clock cycles after a response for the data-write command is received. This occurs even if the command path detects a response error or a cyclic redundancy check (CRC) error in a response. If no response is received from the card until the response timeout, no data are transmitted. Depending on the value of the SDHOST_TRANSFER_MODE bit in SDHOST_CMD_REG register, the data-transmit state machine adds data to the card’s data bus in a stream or in block(s). The data transmit state machine is shown in Figure 34.4-3.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)