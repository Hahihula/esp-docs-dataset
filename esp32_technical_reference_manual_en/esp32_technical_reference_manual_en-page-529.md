**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Table of Data/Remote Frames Description**

- **IDE**: The IDE (Identifier Extension) bit indicates whether the message is SFF (Dominant) or EFF (Recessive). This means that a SFF frame will always win arbitration over an EFF frame given they have the same Base ID.
  
- **ExtID**: The Extended ID (ID.17 to ID.0) is the remaining 8-bits of the 29-bit identifier for EFF.

- **r1**: The r1 (reserved bit 1) is always Dominant.

- **r0**: The r0 (reserved bit 0) is always Dominant.

- **DLC**: The DLC (Data Length Code) is 4-bits and should have a value from 0 to 8. Data Frames use the DLC to indicate the number of data bytes in the Data Frame. Remote Frames used the DLC to indicate the number of data bytes to request from another node.
  
- **Data Bytes**: The data payload of Data Frames. The number of bytes should match the value of DLC. Data byte O is transmitted first, and each data byte is transmitted most significant bit first.

- **CRC Sequence**: The CRC sequence is a 15-bit cyclic redundancy code.

- **CRC Delim**: The CRC Delim (CRC delimiter) is a single Recessive bit that follows the CRC sequence.
  
- **ACK Slot**: The ACK slot (Acknowledgment Slot) intended for Receiver nodes to indicate that the Data or Remote Frame was received without issue. The Transmitter node will send a Recessive bit in the ACK slot and Receiver nodes should override the ACK slot with a Dominant bit if the frame was received without error.

- **ACK Delim**: The ACK Delim (Acknowledgment delimiter) is a single Recessive bit.
  
- **EOF**: The EOF (End of Frame) marks the end of Data or Remote Frame, and consists of seven Recessive bits.

**Subsection Title:**
25.3.2.2 Error and Overload Frames

**Subsection Content - Error Frames**

Error Frames are transmitted when a node detects a Bus Error. Error Frames notably consist of an Error Flag which is made up of 6 consecutive bits of the same value, thus violating the bit-stuffing rule. Therefore, when a particular node detects a Bus Error and transmits an Error Frame, all other nodes will then detect a Stuff Error and transmit their own Error Frames in response. This has the effect of propagating the detection of a Bus Error across all nodes on the bus. When a node detects a Bus Error, it will transmit an Error Frame starting on the next bit. However, if the type of Bus Error was a CRC Error, then the Error Frame will start at the bit following the ACK Delim (see Section 25.3.3). The following Figure **25.3-2** shows the various fields of an Error Frame:

**Figure Title:**
Figure 25.3-2 Various Fields of an Error Frame

**Diagram Description in Table Format**

| Field Name | Length |
| --- | --- |
| Error Frame | - |
| Active/Passive Error Flag (6 bits) | 6 bits |
| Error Flag Superposition (0 to 6 bits) | Variable length within the range specified |
| Error Delimiter (8 bits) | 8 bits |

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32 TRM (Version 5.6)

**Page Numbering and Navigation:**
GoBack
529