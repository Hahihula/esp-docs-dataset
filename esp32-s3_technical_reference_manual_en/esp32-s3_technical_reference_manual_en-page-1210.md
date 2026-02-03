**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Body Text:**

The Error Warning Interrupt is triggered whenever the value of the TWAI_BUS_OFF_ST bit (or the TWAI_ERR_ST bit) changes.

To return to the Error Active state, the TWAI controller must undergo Bus-Off Recovery. Bus-Off Recovery requires the TWAI controller to observe 128 occurrences of 11 consecutive recessive bits on the bus. To initiate Bus-Off Recovery (after entering the Bus-Off state), the TWAI controller should enter Operation Mode by setting the TWAI_RESET_MODE bit to 0. The TEC tracks the progress of Bus-Off Recovery by decrementing the TEC each time when the TWAI controller observes 11 consecutive recessive bits. When Bus-Off Recovery has completed (i.e., TEC has decremented from 127 to 0), the TWAI_BUS_OFF_ST bit will automatically be reset to 0, thus triggering the Error Warning Interrupt.

**Subtitle:**
31.5.8 Error Code Capture

**Body Text:**

The Error Code Capture (ECC) feature allows the TWAI controller to record the error type and bit position of a TWAI bus error in the form of an error code. Upon detecting a TWAI bus error, the Bus Error Interrupt is triggered and the error code is recorded in the TWAI_ERR_CODE_CAP_REG. Subsequent bus errors will trigger the Bus Error Interrupt, but their error codes will not be recorded until the current error code is read from the TWAI_ERR_CODE_CAP_REG.

The following Table 31.5-1 shows the fields of the TWAI_ERR_CODE_CAP_REG:

**Table Title:**
Table 31.5-1 Bit Information of TWAI_ERR_CODE_CAP_REG (0x30)

| Bit | Reserved | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|-----|----------|-------|-------|-------|-------|-------|-------|-------|-------|
|     | ERRC.1^ |       | ERRCO1^ | DIR2   | SEG.4^3 | SEG.3^3 | SEG.2^3 | SEG.1^3 | SEG.0^3 |
| Reserved | 0        | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |

**Notes:**

- ERRC: The Error Code (ERC) indicates the type of bus error: OO for bit error, O1 for format error, 10 for stuff error, 11 for other types of error.
- DIR: The Direction (DIR) indicates whether the TWAI controller was transmitting or receiving when the bus error occurred: 0 for transmitter, 1 for receiver.
- SEG: The Error Segment (SEG) indicates which segment of the TWAI message (i.e., bit position) the bus error occurred at.

The following Table 31.5-12 shows how to interpret the SEGO to SEG4 bits:

**Table Title:**
Table 31.5-12 Bit Information of Bits SEG.4 - SEG.0

| Bit SEG.4 | Bit SEG.3 | Bit SEG.2 | Bit SEG.1 | Bit SEG.0 |
|-----------|-----------|-----------|-----------|-----------|
| O         | O         |          | 1         |           |
| O         |            | 1         |           |           |
| O         |            | 1         |           |           |
| O         |            | 1         |           |           |
| O         |            | 0         | bit SRTR  |           |
|          |           |           | bit IDE   |           |
| O         |            | 1         |           |           |
| O         |            | 1         |           |           |
| O         |            | 1         |           |           |
| O         |            | 0         | ID.28 ~ ID.21 | Cont'd on next page |

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback