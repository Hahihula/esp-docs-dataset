**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Section Header:**
25.3.2 TWAI Messages

**Body Text:**
TWAI nodes use messages to transmit data, and signal errors to other nodes. Messages are split into various frame types, and some frame types will have different frame formats. The TWAI protocol has the following frame types:

- Data Frames
- Remote Frames
- Error Frames
- Overload Frames
- Interframe Space

The TWAI protocol has the following frame formats:
- Standard Frame Format (SFF) that consists of a 11-bit identifier
- Extended Frame Format (EFF) that consists of a 29-bit identifier

**Subsection Header:**
25.3.2.1 Data Frames and Remote Frames

**Body Text:**
Data Frames are used by nodes to send data to other nodes, and can have a payload of 0 to 8 data bytes.
Remote Frames are used to request a Data Frame with the same Identifier from another node, thus does not contain any data bytes. However, Data Frames and Remote Frames share many common fields.

**Figure Reference:**
Figure 25.3-1 illustrates the fields and sub fields of the different frames and formats.

**Subsection Header:**
Arbitration Field

**Body Text:**
When two or more nodes transmits a Data or Remote Frame simultaneously, the Arbitration Field is used to determine which node will win arbitration of the bus. During the Arbitration Field, if a node transmits a Recessive bit but observes a Dominant bit, this indicates that another node has overridden its Recessive bit.
Therefore, the node transmitting the Recessive bit has lost arbitration of the bus and should immediately become a Receiver.

The Arbitration Field primarily consists of the Frame Identifier that is transmitted most significant bit first. Given that a Dominant bit represents a logical 0, and a Recessive bit represents a logical 1:

- A frame with the smallest ID value will always win arbitration.
- Given the same ID and format, Data Frames will always prevail over RTR Frames.
- Given the same first 11 bits of ID, a Standard Format Data Frame will prevail over an Extended Format Data Frame due to the SRR being recessive.

**Subsection Header:**
Control Field

**Body Text:**
The control field primarily consists of the DLC (Data Length Code) which indicates the number of payload data bytes for a Data Frame, or the number of requested data bytes for a Remote Frame. The DLC is transmitted most significant bit first.

**Subsection Header:**
Data Field

**Body Text:**
The Data Field contains the actual payload data bytes of a Data Frame. Remote Frames do not contain a Data Field.

**Subsection Header:**
CRC Field

**Footer Information:**
Espressif Systems
527 ESP32 TRM (Version 5.6)
Submit Documentation Feedback