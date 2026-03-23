
```markdown
| Bit SEG.4 | Bit SEG.3 | Bit SEG.2 | Bit SEG.1 | Bit SEG.0 | Description                     |
|-----------|-----------|-----------|-----------|-----------|---------------------------------|
| 1         | 1         | 0         | 0         | 0         | CRC delimiter                   |
| 1         | 1         | 0         | 0         | 1         | ACK slot                        |
| 1         | 1         | 0         | 1         | 1         | ACK delimiter                   |
| 1         | 1         | 0         | 1         | 0         | end of frame                    |
| 1         | 0         | 0         | 1         | 0         | intermission                    |
| 1         | 0         | 0         | 0         | 1         | active error flag               |
| 1         | 0         | 1         | 1         | 0         | passive error flag              |
| 1         | 0         | 0         | 1         | 1         | tolerate dominant bits          |
| 1         | 0         | 1         | 1         | 1         | error delimiter                 |
| 1         | 1         | 1         | 0         | 0         | overload flag                   |

Notes:
*   Bit SRTR: under Standard Frame Format.
*   Bit IDE: Identifier Extension Bit, 0 for Standard Frame Format.

## 31.4.9 Arbitration Lost Capture

The Arbitration Lost Capture (ALC) feature allows the TWAI controller to record the bit position where it loses arbitration. When the TWAI controller loses arbitration, the bit position is recorded in `TWAI_ARB LOST CAP_REG` and the Arbitration Lost Interrupt is triggered.

Subsequent losses in arbitration will trigger the Arbitration Lost Interrupt, but will not be recorded in `TWAI_ARB LOST CAP_REG` until the current Arbitration Lost Capture is read from the `TWAI_ERR_CODE_CAP_REG`.

Table 31.4-13 illustrates bits and fields of `TWAI_ERR_CODE_CAP_REG` whilst Figure 31.4-5 illustrates the bit positions of a TWAI message.

Figure 31.4-5. Positions of Arbitration Lost Bits

Table 31.4-13. Bit Information of `TWAI_ARB LOST CAP_REG` (0x2c)

| Bit 31-5 | Bit 4   | Bit 3   | Bit 2   | Bit 1   | Bit 0   |
|----------|---------|---------|---------|---------|---------|
| Reserved | BITNO.4¹ | BITNO.3¹ | BITNO.2¹ | BITNO.1¹ | BITNO.0¹ |

Notes:
*   `BITNO`: Bit Number (`BITNO`) indicates the nth bit of a TWAI message where arbitration was lost.
```