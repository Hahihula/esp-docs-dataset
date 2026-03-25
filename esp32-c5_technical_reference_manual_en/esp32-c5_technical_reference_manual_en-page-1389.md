

```markdown
- Manual mode - When TWAIFD_RX_DATA is read, the read pointer of RX FIFO is NOT incremented. To increment the read pointer, software should write 1 to TWAIFD_RXRPMV. This mode can be used when the RX buffer is read via 8/16/32-bit access, since it allows reading a single RX buffer memory word via 4 x 8 bit or 2 x 16 bit access.

RX buffer mode is configured by TWAIFD_RXBAM bit. CAN frame format within the RX buffer is visualized in Figure 38.3-12, which illustrates the alternative CAN frame formats (mutually exclusive) that may be stored in the RX buffer. The CAN frame within the RX buffer spans from 4 to 20 memory words. Its size is given as:

Size of RX frame in words = 4 + ceil(Data field length/4)
```

![Figure 38.3-12: RX buffer](image)

```markdown
### 38.3.9.1 Frame Count

The RX buffer contains a counter of CAN frames. This counter can be read from TWAIFD_RXFRC register. Counter value increments when a frame is stored to the RX buffer and decremented when the last word of a CAN frame is read from the RX buffer.

### 38.3.9.2 RX Buffer Memory

RX buffer memory provides the following status information:

- Number of free memory words, readable from TWAIFD_RX_FREE.
- Write pointer position, readable from TWAIFD_RX_WPP.
- Read pointer position, readable from TWAIFD_RX_RPP.
```

```markdown
Espressif Systems

1389

ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```