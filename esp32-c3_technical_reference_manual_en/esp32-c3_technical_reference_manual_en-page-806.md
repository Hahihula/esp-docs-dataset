

```markdown
|Bit 31-8|Bit 7|Bit 6|Bit 5|Bit 4|Bit 3|Bit 2|Bit 1|Bit 0|
|:--------|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:------|
|Reserved|ID.28|ID.27|ID.26|ID.25|ID.24|ID.23|ID.22|ID.21|
```


Table 31.4-9. TX/RX Identifier 3 (EFF); TWAI Address 0x4c

|Bit 31-8|Bit 7|Bit 6|Bit 5|Bit 4|Bit 3|Bit 2|Bit 1|Bit 0|
|:--------|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:------|
|Reserved|ID.12|ID.11|ID.10|ID.9|ID.8|ID.7|ID.6|ID.5|

```markdown
Table 31.4-10. TX/RX Identifier 4 (EFF); TWAI Address 0x50

|Bit 31-8|Bit 7|Bit 6|Bit 5|Bit 4|Bit 3|Bit 2|Bit 1|Bit 0|
|:--------|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:------|
|Reserved|ID.4|ID.3|ID.2|ID.1|ID.0|X¹|X²|    |
```


Notes:

1. Don’t care. Recommended to be compatible with receive buffer (i.e., set to RTR) in case of using the self reception functionality (or together with self-test functionality).

2. Don’t care. Recommended to be compatible with receive buffer (i.e., set to 0) in case of using the self reception functionality (or together with self-test functionality).

31.4.4.4 Frame Data

The Frame Data field contains the payloads of transmitted or received data frame, and can range from 0 to eight bytes. The number of valid bytes should be equal to the DLC. However, if the DLC is larger than eight bytes, the number of valid bytes would still be limited to eight. Remote frames do not have data payloads, so their Frame Data fields will be unused.

For example, when transmitting a data frame with five bytes, the CPU should write five to the DLC field, and then write data to the corresponding register of the first to the fifth data field. Likewise, when the CPU receives a data frame with a DLC of five data bytes, only the first to the fifth data byte will contain valid payload data for the CPU to read.

31.4.5 Receive FIFO and Data Overruns

The Receive FIFO is a 64-byte internal buffer used to store received messages in First In First Out order. A single received message can occupy between 3 to 13 bytes of space in the Receive FIFO, and their endianness is identical to the register layout of the Receive Buffer registers. The Receive Buffer registers are mapped to the bytes of the first message in the Receive FIFO.

When the TWAI controller receives a message, it will increment the value of `TWAI_RX_MESSAGE_COUNTER` up to a maximum of 64. If there is adequate space in the Receive FIFO, the message contents will be written into
```