**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Section Header:**
TX and RX FIFOs.

**Subsection Heading:**
32.3.3 FIFO and Queue Organization

**Body Text:**
The FIFOs in OTG_FS are primarily used to hold data packet payloads (the data field of USB Data packets). TX FIFOs are used to store data payloads that will be transmitted by OUT transactions in Host mode or IN transactions in Device mode. RX FIFOs are used to store received data payloads of IN transactions in Host mode or OUT transactions in Device mode. In addition to storing data payloads, RX FIFOs also store a `status entry` for each data payload. Each status entry contains information about a data payload such as channel number, byte count, and validity status. When operating in slave mode, status entries are also used to indicate various channel events.

The portion of SPRAM that can be used for FIFO allocation has a depth of 256 and a width of 35 bits (32 data bits plus 3 control bits). The multiple FIFOs used by each channel (in Host mode) or endpoint (in Device mode) are allocated into the SPRAM and can be dynamically sized.

**Subsection Heading:**
32.3.3.1 Host Mode FIFOs and Queues

**Body Text:**
The following FIFOs are used when operating in Host mode (see Figure 32.3-3):

- **Non-periodic TX FIFO:** Stores data payloads of bulk and control OUT transactions for all channels.
- **Periodic TX FIFO:** Stores data payloads of interrupt or isochronous OUT transactions for all channels.
- **RX FIFO:** Stores data payloads of all IN transactions, and status entries that are used to indicate size of data payloads and transaction/channel events such as transfer complete or channel halted.

**Figure Caption:**
Figure 32.3-3. Host Mode FIFOs

**Body Text (continued):**
In addition to FIFOs, Host mode also contains two request queues used to queue up the various transaction requests from the multiple channels. Each entry in a request queue holds the IN/OUT channel number along with other information to perform the transaction such as transaction type). Request queues are also used to queue other types of requests such as a channel halt request.

Unlike FIFOs, request queues are fixed in size and cannot be accessed directly by software. Rather, once a

**Footer:**
Espressif Systems
1231 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback