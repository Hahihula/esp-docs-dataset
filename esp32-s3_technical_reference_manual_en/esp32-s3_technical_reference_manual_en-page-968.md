**Title:**
Chapter 26 UART Controller (UART)

**Header:**
GoBack

**Register Information:**
- **Register Name:** UHCI_CONF1_REG (0x0018)
- **Address Bits:** [31, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0] with corresponding labels from top to bottom: "Reset", etc.

**Field Descriptions and Functions in the Register (with register address bits indicated):**

- **UHCI_CHECK_SUM_EN**
  - Description: This is the enable bit to check header checksum when UHCI receives a data packet. 
  - Access Type: Read/Write

- **UHCI_CHECK_SEQ_EN**
  - Description: This is the enable bit to check sequence number when UHCI receives a data packet.
  - Access Type: Read/Write

- **UHCI_CRC_DISABLE**
  - Description: Set this bit to support CRC calculation. Data Integrity Check Present bit in UHCI packet frame should be 1.
  - Access Type: Read/Write

- **UHCI_SAVE_HEAD**
  - Description: Set this bit to save the packet header when UHCI receives a data packet.
  - Access Type: Read/Write

- **UHCI_TX_CHECK_SUM_RE**
  - Description: Set this bit to encode the data packet with a checksum.
  - Access Type: Read/Write

- **UHCI_TX_ACK_NUM_RE**
  - Description: Set this bit to encode the data packet with an acknowledgment when a reliable packet is to be transmitted.
  - Access Type: Read/Write

- **UHCI_WAIT_SW_START**
  - Description: The UHCI encoder will jump to ST_SW_WAIT status if this bit is set to 1. 
  - Access Type: Read/Write

- **UHCI_SW_START**
  - Description: If current UHCI_ENCODE_STATE is ST_SW_WAIT, the UHCI will start to send data packet out when this bit is set to 1.
  - Access Type: Read/Write (SC)

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Title: ESP32-S3 TRM (Version 1.7)
- Page Number: 968

**Link:**
Submit Documentation Feedback