**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
GoBack

**Register Information and Description:**

1. **Register Name:** UHCI_STATE0_REG (0x001C)
   - **Description:** This field indicates the error type when DMA has received a packet with error.
     - **Field Details:**
       - 3'b001: Checksum error in the HCI packet
       - 3'b010: Sequence number error in the HCI packet
       - 3'b011: CRC bit error in the HCI packet
       - 3'b100: 0xCO is found but the received HCI packet is not end.
       - 3'b101: 0xCO is not found when the HCI packet has been received.

2. **Register Name:** UHCI_DECODE_STATE (PO)
   - **Description:** UHCI decoder status

3. **Register Name:** UHCI_STATE1_REG (0x0020)
   - **Description:** UHCI encoder status
     - This register stores the header of the current received packet.

4. **Register Name:** UHCI_RX_HEAD_REG (0x003C)
   - **Description:** This register stores the header of the current received packet

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
983 ESP32-S3 TRM (Version 1.7)