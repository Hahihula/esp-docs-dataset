

```markdown
|Bit 31-8|Bit 7|Bit 6|Bit 5|Bit 4|Bit 3|Bit 2|Bit 1|Bit 0|
|:--------|:-------|:-------|:------|:------|:------|:------|:-------|:-------|
|Reserved|ERRC.1¹|ERRCO¹|DIR²|SEG.4³|SEG.3³|SEG.2³|SEG.1³|SEG.O³|

Notes:
*   ERRC: The Error Code (ERRC) indicates the type of bus error: 00 for bit error, 01 for format error, 10 for stuff error, and 11 for other types of error.
*   DIR: The Direction (DIR) indicates whether the TWAI controller was transmitting or receiving when the bus error occurred: 0 for transmitter, 1 for receiver.
*   SEG: The Error Segment (SEG) indicates which segment of the TWAI message (i.e., bit position) the bus error occurred at.

The following Table 31.4-12 shows how to interpret the SEG.O to SEG.4 bits.

Table 31.4-12. Bit Information of Bits SEG.4 - SEG.O

|Bit SEG.4|Bit SEG.3|Bit SEG.2|Bit SEG.1|Bit SEG.0|Description|
|:--------|:---------|:----------|:----------|:----------|:------------|
|0        |0         |0          |1          |1          |start of frame|
|0        |0         |0          |1          |0          |ID.28 ~ ID.21|
|0        |0         |1          |1          |0          |ID.20 ~ ID.18|
|0        |0         |1          |0          |0          |bit SRTR|
|0        |0         |1          |0          |1          |bit IDE|
|0        |0         |1          |1          |1          |ID.17 ~ ID.13|
|0        |1         |1          |1          |1          |ID.12 ~ ID.5|
|0        |1         |1          |1          |0          |ID.4 ~ ID.0|
|0        |1         |1          |0          |0          |bit RTR|
|0        |1         |1          |0          |1          |reserved bit 1|
|0        |1         |0          |0          |1          |reserved bit 0|
|0        |1         |0          |1          |1          |data length code|
|0        |1         |0          |1          |0          |data field|
|0        |1         |0          |0          |0          |CRC sequence|

Cont'd on next page
```