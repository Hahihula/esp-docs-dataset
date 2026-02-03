**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Table Header:**
Data/Remote Frames | Description

- **IDE**: The IDE (Identifier Extension) bit indicates whether the message is SFF (dominant or EFF (recessive). This means that a SFF frame will always win arbitration over an EFF frame given they have the same Base ID.
  
- **ExtId**: The Extended ID (ID.17 to ID.0) is the remaining 8-bits of the 29-bit identifier for EFF.

- **r1**: The r1 bit (reserved bit 1) is always dominant.

- **r0**: The r0 bit (reserved bit 0) is always dominant.

- **DLC**: The DLC (Data Length Code) is 4-bit long and should contain any value from 0 to 8. Data frames use the DLC to indicate the number of data bytes in the data frame. Remote frames used the DLC to indicate the number of data bytes to request from another node.
  
- **Data Bytes**: The data payload of data frames. The number of bytes should match the value of DLC. Data byte O is transmitted first, and each data byte is transmitted from the most significant bit first.

- **CRC Sequence**: The CRC sequence is a 15-bit cyclic redundancy code.

- **CRC Delim**: The CRC Delim (CRC Delimiter) is a single recessive bit that follows the CRC sequence.
  
- **ACK Slot**: The ACK Slot (Acknowledgment Slot) is intended for receiver nodes to indicate that the data or remote frame was received without an issue. The transmitter will send a recessive bit in the ACK Slot and receiver nodes should override the ACK Slot with a dominant bit if the frame was received without errors.

- **ACK Delim**: The ACK Delim (Acknowledgment Delimiter) is a single recessive bit.
  
- **EOF**: The EOF (End of Frame) marks the end of data or remote frame, and consists of seven recessive bits.

**Subsection Title:**
31.3.2.2 Error and Overload Frames

**Subsection Subtitle:**
Error Frames

**Body Text:**
Error frames are transmitted when a node detects a bus error. Error frames notably consist of an Error Flag which is made up of 6 consecutive bits of the same value, thus violating the bit-stuffing rule. Therefore, when a particular node detects a bus error and transmits an error frame, all other nodes will then detect a stuff error and transmit their own error frames in response. This has the effect of propagating the detection of a bus error across all nodes on the bus.

When a node detects a bus error, it will transmit an error frame starting from the next bit. However, if the type of bus error was a CRC error, then the error frame will start at the bit following the ACK Delim (see Section 31.3.3 for more details). The following Figure 31.3-2 shows different fields of an error frame:

**Figure Title:**
Figure 31.3-2. Fields of an Error Frame

**Figure Description in Table Format:**

| Field Name | Bits |
| --- | --- |
| Error Frame | (6 bits) |
| Active/Passive Error Flag | (6 bits) |
| Error Flag Superposition | (0 to 6 bits) |
| Error Delimiter | (8 bits) |

**Footer Information:**
Espressif Systems  
1189  
ESP32-S3 TRM (Version 1.7)

**Action Links:**
Submit Documentation Feedback