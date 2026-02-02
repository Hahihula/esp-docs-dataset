**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Section Heading:**
GoBack

**Body Text with Descriptions and Definitions of Bits in Table 25.5-12**

- **DIR:** The Direction (DIR) indicates whether the TWAI controller was transmitting or receiving when the bus error occurred, where:
  - `0` for Transmitter
  - `1` for Receiver

- **SEG:** The Error Segment (SEG) indicates which segment of the TWAI message is being reported as an error. This can be determined by interpreting the SEG.O to SEG.4 bits.

**Table Title:**
Table 25.5-12. Bit Information of Bits SEG.4 - SEG.0

| Bit SEG.4 | Bit SEG.3 | Bit SEG.2 | Bit SEG.1 | Bit SEG.0 | Description |
|-----------|-----------|-----------|-----------|-----------|-------------|
| `0`       | `0`       | `0`       | `1`       | `1`       | start of frame |
| `0`       | `0`       | `1`       | `1`       | `0`       | ID.28 to ID.21 |
| `0`       | `1`       | `0`       | `1`       | `0`       | ID.20 to ID.18 |
| `0`       | `1`       | `1`       | `1`       | `0`       | bit SRTR¹      |
| `0`       | `0`       | `1`       | `1`       | `1`       | bit IDE²      |
| `0`       | `1`       | `1`       | `1`       | `1`       | ID.17 to ID.13 |
| `0`       | `1`       | `1`       | `1`       | `1`       | ID.12 to ID.5  |
| `0`       | `1`       | `1`       | `1`       | `0`       | ID.4 to ID.0   |
| `0`       | `1`       | `1`       | `1`       | `0`       | bit RTR       |
| `0`       | `1`       | `1`       | `1`       | `0`       | reserved bit 1|
| `0`       | `1`       | `1`       | `1`       | `0`       | reserved bit O|
| `0`       | `1`       | `1`       | `1`       | `1`       | data length code |
| `0`       | `1`       | `1`       | `1`       | `0`       | data field    |
| `0`       | `1`       | `1`       | `1`       | `0`       | CRC sequence  |
| `0`       | `1`       | `1`       | `1`       | `0`       | CRC delimiter  |
| `1`       | `1`       | `1`       | `0`       | `0`       | acknowledge slot|
| `1`       | `1`       | `1`       | `0`       | `1`       | acknowledge delimiter|
| `1`       | `1`       | `1`       | `0`       | `1`       | end of frame   |
| `1`       | `1`       | `0`       | `0`       | `0`       | intermission  |
| `1`       | `1`       | `0`       | `0`       | `1`       | active error flag|
| `1`       | `1`       | `0`       | `0`       | `1`       | passive error flag|
| `1`       | `1`       | `0`       | `0`       | `1`       | tolerate dominant bits |
| `1`       | `1`       | `0`       | `0`       | `1`       | error delimiter|
| `1`       | `1`       | `0`       | `0`       | `0`       | overload flag |

**Notes:**
- Bit RTR: under Standard Frame Format.
- Identifier Extension Bit: 0 for Standard Frame Format.

**Subsection Title and Description with Additional Information on Arbitration Lost Capture (ALC):**

25.5.9 Arbitration Lost Capture

The Arbitration Lost Capture (ALC) feature allows the TWAI controller to record the bit position where it loses arbitration when:
- The TWAI controller is losing arbitration.
- When this occurs, the bit position information will be recorded in `TWAI_ARB_LOST_CAP_REG` and the Arbitration Lost Interrupt is triggered.

Subsequent losses of arbitration trigger the Arbitration Lost Interrupt but are not automatically written into `TWAI_ARB_LOST_CAP_REG` until:
- The current Arbitration Lost Capture value has been read from it by a subsequent loss event. 

**Footer:**
Espressif Systems
548 ESP32 TRM (Version 5.6)
Submit Documentation Feedback