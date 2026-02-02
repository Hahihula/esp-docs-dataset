**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Body Text with List Items and Diagram Description:**

- Configures clock parameters
- Configures card command parameters
- Sends commands to card bus (ccmd_out line)
- Receives responses from card bus (ccmd_in line)
- Sends responses to BIU
- Drives the P-bit on the command line

The command path State Machine is shown in Figure 27.4-2.

**Figure Caption:**
Figure 27.4-2. Command Path State Machine

**Diagram Description of "Command Path State Machine":**

- Transmit, response_expected=0
- Load_new_cmd
- INCC done
- Send IRQ Response
- Receive response
- wait_busy
- response_expected=1
- response_timeout

**Subsection Title:**
27.4.3 Data Path

**Body Text for "Data Path":**

The data path block pops FIFO data and transmits them on cdata_out during a write-data transfer, or it receives data on cdata_in and pushes them into FIFO during a read-data transfer. The data path loads new data parameters, i.e., expected data, read/write data transfer, stream/block transfer, block size, byte count, card type, timeout registers, etc., whenever a data transfer command is not in progress.

If the data_expected bit is set in the Command register, the new command is a data-transfer command and the data path starts one of the following operations:

- Transmitting data if the read/write bit = 1
- Receiving data if read/write bit = 0

**Subsection Title:**
27.4.3.1 Data Transmit Operation

**Body Text for "Data Transmit Operation":**

The data transmit state machine is illustrated in Figure 27.4-3. The module starts data transmission two clock cycles after a response for the data-write command is received. This occurs even if the command path detects a response error or a cyclic redundancy check (CRC) error in a response. If no response is received from the card until the response timeout, no data are transmitted. Depending on the value of the transfer_mode bit in the Command register, the data-transmit state machine adds data to the card’s data bus in a stream or in block(s). The data transmit state machine is shown in Figure 27.4-3.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)