**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Heading:**
31.5.4.2 Frame Information

**Body Text:**
The frame information is one byte long and specifies a message’s frame type, frame format, and length of data. The frame information fields are shown in Table 31.5-4.

**Table Title (with headers):**
Table 31.5-4. TX/RX Frame Information (SFF/EFF); TWAI Address 0x40

| Bit | Description |
|-----|-------------|
| Bit 31-8 | Reserved |
| Bit 7 | RTR² |
| Bit 6 | RTR² |
| Bit 5 | X³ |
| Bit 4 | DLC.3⁴ |
| Bit 3 | DLC.2⁴ |
| Bit 2 | DLC.1¹⁴ |
| Bit 1 | DLC.0¹⁴ |
| Bit 0 | Reserved |

**Notes:**
1. FF: The Frame Format (FF) bit specifies whether the message is Extended Frame Format (EFF) or Standard Frame Format (SFF). The message is EFF when FF bit is 1, and SFF when FF bit is 0.
2. RTR: The Remote Transmission Request (RTR) bit specifies whether the message is a data frame or a remote frame. The message is a remote frame when the RTR bit is 1, and a data frame when the RTR bit is 0.
3. X: Don’t care, can be any value.
4. DLC: The Data Length Code (DLC) field specifies the number of data bytes for a data frame, or the number of data bytes to request in a remote frame. TWAI data frames are limited to a maximum payload of 8 data bytes, and thus the DLC should range anywhere from 0 to 8.

**Section Heading:**
31.5.4.3 Frame Identifier

**Body Text:**
The Frame Identifier fields is two-byte (11-bit) long if the message is SFF, and four-byte (29-bit) long if the message is EFF.
The Frame Identifier fields for an SFF (11-bit) message is shown in Table 31.5-5.

**Table Title:**
Table 31.5-4. TX/RX Identifier 1 (SFF); TWAI Address 0x44

| Bit | Description |
|-----|-------------|
| Bit 31-8 | Reserved |
| Bit 7 | ID.10 |
| Bit 6 | ID.9 |
| Bit 5 | ID.8 |
| Bit 4 | ID.7 |
| Bit 3 | ID.6 |
| Bit 2 | ID.5 |
| Bit 1 | ID.4 |
| Bit 0 | ID.3 |

**Table Title:**
Table 31.5-6. TX/RX Identifier 2 (SFF); TWAI Address 0x48

| Bit | Description |
|-----|-------------|
| Bit 31-8 | Reserved |
| Bit 7 | ID.2 |
| Bit 6 | ID.1 |
| Bit 5 | ID.0¹ |
| Bit 4 | X¹² |
| Bit 3 | X²⁴ |
| Bit 2 | X²⁴ |
| Bit 1 | X²⁴ |
| Bit 0 | X²⁴ |

**Notes:**
1. Don’t care. Recommended to be compatible with receive buffer (i.e., set to RTR) in case of using the self reception functionality (or together with self-test functionality).

**Footer Information:**
Espressif Systems
1204 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback