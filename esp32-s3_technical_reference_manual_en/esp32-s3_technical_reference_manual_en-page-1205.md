**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section with Table and Notes:**

- **Title:** The Frame Identifier fields for an EFF (29-bits) message is shown in Table 31.5-7, 31.5-10.

- **Table Title:** Table 31.5-7. TX/RX Identifier 1 (EFF); TWAI Address 0x44

| Bit | Reserved | ID.28 | ID.27 | ID.26 | ID.25 | ID.24 | ID.23 | ID.22 | ID.21 |
|-----|----------|-------|-------|-------|-------|-------|-------|-------|-------|
| 31-8 | Bit 7    |       |       |       |       |       |       |       |       |

- **Table Title:** Table 31.5-8. TX/RX Identifier 2 (EFF); TWAI Address 0x48

| Bit | Reserved | ID.20 | ID.19 | ID.18 | ID.17 | ID.16 | ID.15 | ID.14 | ID.13 |
|-----|----------|-------|-------|-------|-------|-------|-------|-------|-------|
| 31-8 | Bit 7    |       |       |       |       |       |       |       |       |

- **Table Title:** Table 31.5-9. TX/RX Identifier 3 (EFF); TWAI Address 0x4c

| Bit | Reserved | ID.12 | ID.11 | ID.10 | ID.9 | ID.8 | ID.7 | ID.6 | ID.5 |
|-----|----------|-------|-------|-------|-----|-----|-----|-----|-----|
| 31-8 | Bit 7    |       |       |       |     |     |     |     |     |

- **Table Title:** Table 31.5-10. TX/RX Identifier 4 (EFF); TWAI Address 0x50

| Bit | Reserved | ID.4 | ID.3 | ID.2 | ID.1 | ID.0 | X^1 | X^2 |
|-----|----------|------|------|------|------|------|-----|-----|
| 31-8 | Bit 7    |       |       |       |     |     |     |     |

**Notes:**
1. Don't care. Recommended to be compatible with receive buffer (i.e., set to RTR) in case of using the self reception functionality (or together with self-test functionality).
2. Don't care. Recommended to be compatible with receive buffer (i.e., set to 0) in case of using the self reception functionality (or together with self-test functionality).

**Subsection Title:**
31.5.4.4 Frame Data

- **Body Text:** The Frame Data field contains the payloads of transmitted or received data frame, and can range from 0 to eight bytes. The number of valid bytes should be equal to the DLC. However, if the DLC is larger than eight, the number of valid bytes would still be limited to eight. Remote frames do not have data payloads, thus their Frame Data fields will be unused.

- **Example:** For example, when transmitting a data frame with five bytes, the CPU should write five to the DLC field, and then write data to the corresponding register of the first to the fifth data field. Likewise, when receiving a data frame with a DLC of five data bytes, only the first to the fifth data byte will contain valid payload data for the CPU to read.

**Subsection Title:**
31.5.5 Receive FIFO and Data Overruns

- **Body Text:** The Receive FIFO is a 64-byte internal buffer used to store received messages in First In First Out order. A single received message can occupy between three to 13 bytes of space in the Receive FIFO, and their...

**Footer:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)