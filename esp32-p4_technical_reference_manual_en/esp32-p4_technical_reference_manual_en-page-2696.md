

```markdown
|Bit 31-8|Bit 7|Bit 6|Bit 5|Bit 4|Bit 3|Bit 2|Bit 1|Bit 0|
|:--------|:-----|:------|:-----|:-----|:-------|:-------|:-------|:-------|
|Reserved|FF¹|RTR²|X³|   |DLC.3⁴|DLC.2⁴|DLC.1⁴|DLC.0⁴|

Notes:
1. FF: The Frame Format (FF) bit specifies whether the message is Extended Frame Format (EFF) or Standard Frame Format (SFF). The message is EFF when the FF bit is 1, and SFF when the FF bit is 0.
2. RTR: The Remote Transmission Request (RTR) bit specifies whether the message is a data frame or a remote frame. The message is a remote frame when the RTR bit is 1, and a data frame when the RTR bit is 0.
3. X: Don’t care, can be any value.
4. DLC: The Data Length Code (DLC) field specifies the number of data bytes for a data frame, or the number of data bytes to request in a remote frame. TWAI data frames are limited to a maximum payload of 8 data bytes, and thus the DLC should range from 0 to 8.
```

### 53.4.3.3 Frame Identifier

The Frame Identifier fields occupy two-byte (11-bit) long if the message is SFF, and four-byte (29-bit) long if the message is EFF.

The Frame Identifier fields for an SFF (11-bit) message are shown in Table 53.4-5 ~ 53.4-6.

```markdown
Table 53.4-5. TX/RX Identifier 1 (SFF); TWAI Address 0x44

|Bit 31-8|Bit 7|Bit 6|Bit 5|Bit 4|Bit 3|Bit 2|Bit 1|Bit 0|
|:--------|:-----|:-----|:-----|:-----|:------|:-----|:-----|:-----|
|Reserved|ID.10|ID.9|ID.8|ID.7|ID.6|ID.5|ID.4|ID.3|

Table 53.4-6. TX/RX Identifier 2 (SFF); TWAI Address 0x48

|Bit 31-8|Bit 7|Bit 6|Bit 5|Bit 4|Bit 3|Bit 2|Bit 1|Bit 0|
|:--------|:-----|:-----|:-----|:-----|:------|:-----|:-----|:-----|
|Reserved|ID.2|ID.1|ID.0|X¹|X²|X²|    |    |
```

Notes:
1. Don’t care. Recommended to be compatible with receive buffer (i.e., set to RTR) in case of using the self-reception functionality (or together with self-test functionality).
```