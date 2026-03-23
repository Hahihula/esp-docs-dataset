

```markdown
## 33.4.4.2 Frame Information

The frame information is one byte long and specifies a message's frame type, frame format, and length of data. The frame information fields are shown in Table 33.4-4.

Table 33.4-4. TX/RX Frame Information (SFF/EFF)□TWAI Address 0x40

| Bit 31-8 | Bit 7   | Bit 6 | Bit 5 | Bit 4 | Bit 3    | Bit 2 | Bit 1 | Bit 0 |
|----------|---------|-------|-------|-------|----------|-------|-------|-------|
| Reserved | FF¹     | RTR²  | X³    | X³    | DLC.3⁴    | DLC.2⁴ | DLC.1⁴ | DLC.0⁴ |

**Notes:**
1. FF: The Frame Format (FF) bit specifies whether the message is Extended Frame Format (EFF) or Standard Frame Format (SFF). The message is EFF when FF bit is 1, and SFF when FF bit is 0.
2. RTR: The Remote Transmission Request (RTR) bit specifies whether the message is a data frame or a remote frame. The message is a remote frame when the RTR bit is 1, and a data frame when the RTR bit is 0.
3. X: Don't care, can be any value.
4. DLC: The Data Length Code (DLC) field specifies the number of data bytes for a data frame, or the number of data bytes to request in a remote frame. TWAI data frames are limited to a maximum payload of 8 data bytes, and thus the DLC should range anywhere from 0 to 8.

## 33.4.4.3 Frame Identifier

The Frame Identifier fields occupies two-byte (11-bit) long if the message is SFF, and four-byte (29-bit) long if the message is EFF.

The Frame Identifier fields for an SFF (11-bit) message is shown in Table 33.4-5 ~ 33.4-6.

Table 33.4-5. TX/RX Identifier 1 (SFF); TWAI Address 0x44

| Bit 31-8 | Bit 7   | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|----------|---------|-------|-------|-------|-------|-------|-------|-------|
| Reserved | ID.10   | ID.9  | ID.8  | ID.7  | ID.6  | ID.5  | ID.4  | ID.3  |

Table 33.4-6. TX/RX Identifier 2 (SFF); TWAI Address 0x48

| Bit 31-8 | Bit 7   | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|----------|---------|-------|-------|-------|-------|-------|-------|-------|
| Reserved | ID.2    | ID.1  | ID.0  | X¹    | X²    | X²    | X²    | X²    |

**Notes:**
1. Don't care. Recommended to be compatible with receive buffer (i.e., set to RTR) in case of using the self reception functionality (or together with self-test functionality).
2. Don't care. Recommended to be compatible with receive buffer (i.e., set to 0) in case of using the self reception functionality (or together with self-test functionality).

The Frame Identifier fields for an EFF (29-bits) message is shown in Table 33.4-7 ~ 33.4-10.

Table 33.4-7. TX/RX Identifier 1 (EFF); TWAI Address 0x44
```