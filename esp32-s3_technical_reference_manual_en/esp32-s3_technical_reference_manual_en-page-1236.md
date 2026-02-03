**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Table Title and Number:**
Table 32.3-1. IN and OUT Transactions in Slave Mode

**Sections with Subheadings, Lists, or Tables:**

### Host Mode - OUT Transactions:
1. Software specifies the size of the data packet and the number of data packets (1 data packet) in the USB_HCTSIZn_REG register, enables the channel, then copies the packet’s data payload into the TX FIFO.
2. When the last DWORD of the data payload has been pushed, the controller core will automatically write a request into the appropriate request queue.

3. If the transaction was successful,
   - The received packet will be pushed into the RX FIFO along with a packet status entry.
   - If the transaction was unsuccessful (e.g., due to full RX FIFO), the endpoint will automatically NAK the incoming packet, an error interrupt USB_H_NACKn will occur.

### Device Mode:
1. Software specifies the expected size of the data packet (1 MPS) and the number of data packets (1 data packet) in the USB_DIEPTSIZn_REG register.
2. Once the endpoint is enabled, it will wait for the host to transmit a packet to it.

3. The received packet will be pushed into the RX FIFO along with a packet status entry.
   - If the transaction was unsuccessful,
     - When an error interrupt (e.g., full RX FIFO), the endpoint will automatically NAK the incoming packet; USB_H_NACKn will occur

### IN Transactions:
1. Software specifies the expected size of the data packet and the number of packets (1 data packet) in the USB_HCTSIZn_REG register, then enables the channel.
2. The controller core will automatically write a request into the appropriate request queue.

3. If the transaction was successful,
   - When the packet has been transmitted, the USB_XFERCOMPL interrupt will be generated; if unsuccessful and an error interrupt (e.g., full RX FIFO), USB_H_NACKn will occur

### Additional Information:
When operating at the transfer level in Slave mode, one or more transaction-level operations can be pipelined thus being analogous to transfer level operation in DMA mode. Within pipelined transactions, multiple packets of the same transfer can be read/written from the FIFOs in single instance; therefore preventing the need for interrupting software on a per-packet basis.

Operating on a transfer level in Slave mode is similar to operating at the transaction-level except that:
- The transfer size and packet count are specified by setting USB_HCTSIZn_REG or USB_DIEPTSIZn_REG register.
- After channel or endpoint enable, multiple data packets worth of payloads should be written to or read from TX or RX FIFOs respectively (given there is enough space).

**Footer:**
Espressif Systems
1236 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback