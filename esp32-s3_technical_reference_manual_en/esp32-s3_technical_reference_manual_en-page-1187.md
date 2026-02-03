**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Header:**
31.3.2 TWAI Messages

**Body Text:**
TWAI nodes use messages to transmit data, and signal errors to other nodes. Messages are split into various frame types, and some frame types will have different frame formats.

The TWAI protocol has the following frame types:
- Data frames
- Remote frames
- Error frames
- Overload frames
- Interframe space

**Subsection Header:**
31.3.2 The TWAI protocol has the following frame formats:

**List Items under Subsection:**
- Standard Frame Format (SFF) that consists of a 11-bit identifier
- Extended Frame Format (EFF) that consists of a 29-bit identifier

**Subsection Header:**
31.3.2.1 Data Frames and Remote Frames

**Body Text:**
Data frames are used by nodes to send data to other nodes, and can have a payload of 0 to 8 data bytes.
Remote frames are used for nodes to request a data frame with the same identifier from another node, thus they do not contain any data bytes. However, data frames and remote frames share many common fields.

**Figure Reference:**
Figure 31.3-1 illustrates the fields and sub-fields of different frames and formats.

**Subsection Header:**
Arbitration Field

**Body Text:**
When two or more nodes transmits a data or remote frame simultaneously, the arbitration field is used to determine which node will win arbitration of the bus. During the arbitration field, if a node transmits a recessive bit while observes a dominant bit, this indicates that another node has overridden its recessive bit. Therefore, the node transmitting the recessive bit has lost arbitration of the bus and should immediately switch to be a receiver.

The arbitration field primarily consists of the frame identifier that is transmitted from the most significant bit first. Given that a dominant bit represents a logical 0, and a recessive bit represents a logical 1:

- A frame with the smallest ID value will always win arbitration.
- Given the same ID and format, data frames will always prevail over remote frames.

**Subsection Header:**
Control Field

**Body Text:**
The control field primarily consists of the DLC (Data Length Code) which indicates the number of payload data bytes for a data frame, or the number of requested data bytes for a remote frame. The DLC is transmitted from the most significant bit first.

**Subsection Header:**
Data Field

**Body Text:**
The data field contains the actual payload data bytes of a data frame. Remote frames do not contain a data field.

**Subsection Header:**
CRC Field

**Footer Information:**
Espressif Systems
1187 Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)