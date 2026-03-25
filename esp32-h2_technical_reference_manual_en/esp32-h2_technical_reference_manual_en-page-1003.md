

```markdown
Table 34.4-3 – cont’d from previous page

| Standard Frame Format (SFF) Offset Address | Content                     | Extended Frame Format (EFF) Offset Address | Content                          |
|--------------------------------------------|------------------------------|---------------------------------------------|-----------------------------------|
| 0x64                                       | TX/RX data byte 7            | 0x64                                        | TX/RX data byte 5                 |
| 0x68                                       | TX/RX data byte 8            | 0x68                                        | TX/RX data byte 6                 |
| 0x6c                                       | reserved                     | 0x6c                                        | TX/RX data byte 7                 |
| 0x70                                       | reserved                     | 0x70                                        | TX/RX data byte 8                 |

Table 34.4-4. TX/RX Frame Information (SFF/EFF); TWAI Address 0x40

| Bit 31–8 | Bit 7   | Bit 6 | Bit 5 | Bit 4 | Bit 3     | Bit 2 | Bit 1    | Bit 0 |
|----------|---------|-------|-------|-------|-----------|-------|----------|-------|
| Reserved | FF¹     | RTR²   | X³    | X³    | DLC.3⁴     | DLC.2⁴ | DLC.1⁴   | DLC.0⁴ |

Notes:

1.  FF: The Frame Format (FF) bit specifies whether the message is Extended Frame Format (EFF) or Standard Frame Format (SFF). The message is EFF when the FF bit is 1, and SFF when the FF bit is 0.
2.  RTR: The Remote Transmission Request (RTR) bit specifies whether the message is a data frame or a remote frame. The message is a remote frame when the RTR bit is 1, and a data frame when the RTR bit is 0.
3.  X: Don’t care, can be any value.
4.  DLC: The Data Length Code (DLC) field specifies the number of data bytes for a data frame, or the number of data bytes to request in a remote frame. TWAI data frames are limited to a maximum payload of 8 data bytes, and thus the DLC should range from 0 to 8.
```