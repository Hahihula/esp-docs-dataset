**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Table Header:**
Table 31.5-12 – cont’d from previous page

| Bit SEG.4 | Bit SEG.3 | Bit SEG.2 | Bit SEG.1 | Bit SEG.0 | Description |
|-----------|-----------|-----------|-----------|-----------|-------------|
| O         | 1         | 1         | O         | 0         | bit RTR     |
| O         | 1         | 1         | O         | 1         | reserved bit 1 |
| O         | 1         | 0         | 1         | 1         | reserved bit 0 |
| O         | 1         | 0         | 1         | 1         | data length code |
| O         | 1         | 0         | 1         | 0         | data field   |
| O         | 1         | 0         | 0         | 0         | CRC sequence |
| 1         | 1         | 0         | 0         | 0         | CRC delimiter|
| 1         | 1         | 0         | 0         | 1         | ACK slot     |
| 1         | 1         | O         | 1         | 1         | ACK delimiter|
| 1         | 1         | 0         | 0         | 0         | end of frame |
| 1         | 0         | 0         | 1         | 0         | intermission |
| 1         | 0         | O         | 1         | 1         | active error flag|
| 1         | 0         | 1         | 1         | 0         | passive error flag|
| 1         | 0         | 0         | 1         | 1         | tolerate dominant bits |
| 1         | 0         | O         | 1         | 1         | error delimiter|
| 1         | 1         | 1         | 0         | 0         | overload flag |

**Notes:**
- Bit SRTR: under Standard Frame Format.
- Bit IDE: Identifier Extension Bit, 0 for Standard Frame Format.

**Subsection Title and Description:**
31.5.9 Arbitration Lost Capture

The Arbitration Lost Capture (ALC) feature allows the TWAI controller to record the bit position where it loses arbitration. When the TWAI controller loses arbitration, the bit position is recorded in the TWAI_ARB LOST CAP_REG.

Subsequent losses in arbitration will trigger the Arbitration Lost Interrupt, but will not be recorded in the TWAI_ARB LOST CAP_REG until the current Arbitration Lost Capture is read from the TWAI_ERR_CODE_CAP_REG.

**Table Reference:**
Table 31.5-12 illustrates bits and fields of the TWAI_ERR_CODE_CAP_REG whilst Figure 31.5-5 illustrates the bit positions of a TWAI message.
Table 31.5-13 Bit Information of TWAI_ARB LOST CAP_REG (0x2c)

| Bit 31-5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|----------|-------|-------|-------|-------|-------|
| Reserved | BITNO.4^1 | BITNO.3^1 | BITNO.2^1 | BITNO.1^1 | BITNO.0^1 |

**Notes:**
- BITNO: Bit Number (BITNO) indicates the nth bit of a TWAI message where arbitration was lost.

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback