**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Figure Caption and Diagrams:**

1. **Figure 34.4-3:** Data Transmit State Machine

   - The diagram shows the states of a data transmit state machine with transitions based on various conditions such as "load_new_cmd", "data_expected", etc.

2. **Figure 34.4-4:** Data Receive State Machine

   - Similar to Figure 34.4-3, this figure illustrates another state machine for receiving data from the card's bus in a stream or block(s).

**Subsection Title:**
34.4.3.2 Data Receive Operation

**Body Text:**

The module receives data two clock cycles after the end bit of a data-read command, even if the command path detects a response error or a CRC error. If no response is received from the card and a response timeout occurs, the BIU does not receive a signal about the completion of the data transfer. If the command sent by the CIU is an illegal operation for the card, it would prevent the card from starting a read-data transfer, and the BIU will not receive a signal about the completion of the data transfer.

If no data is received by the data timeout, the data path signals a data timeout to the BIU, which marks an end to the data transfer. Based on the value of the SDHOST_TRANSFER_MODE bit in SDHOST_CMD_REG register, the data-receive state machine gets data from the card's data bus in a stream or block(s). The data receive state machine is shown in Figure 34.4-4.

**Subsection Title:**
34.5 Software Restrictions for Proper CIU Operation

**Body Text:**

- Only one card at a time can be selected to execute a command or data transfer. For example, when data are being transferred to or from a card, a new command must not be issued to another card. A new command, however, can be issued to the same card, allowing it to read the device status or stop the transfer.

- Only one command at a time can be issued for data transfers.

**Footer:**
Espressif Systems
1273

**Link Texts:**
Submit Documentation Feedback

**Document Version Information:** 
ESP32-S3 TRM (Version 1.7)