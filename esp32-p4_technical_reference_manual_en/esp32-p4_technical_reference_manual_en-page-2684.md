

```markdown
Figure 53.2-1. Bit Fields in Data Frames and Remote Frames


CRC Field

The CRC field primarily consists of a CRC sequence. The CRC sequence is a 15-bit cyclic redundancy code calculated from the de-stuffed contents (everything from the SOF to the end of the data field) of a data or remote frame.

ACK Field

The ACK field primarily consists of an ACK Slot and an ACK Delim. The ACK field indicates that the receiver has received an effective message from the transmitter.


Table 53.2-1. Data Frames and Remote Frames in SFF and EFF
```