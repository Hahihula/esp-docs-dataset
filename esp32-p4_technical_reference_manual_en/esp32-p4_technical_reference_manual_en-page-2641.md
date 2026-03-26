
```markdown
Register 52.7. DMAOPERATION_MODE_REG (0x1018)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | FLUSH_TX_FIFO | DIS_DROP_TCPPIP_ERR_FRAM | DIS_FLUSH_RECV_FRAMES | TX_THRESH_CTRL | START_STOP_TRANSMISSION_COMMAND | PWD_ERR_UNDER_GF | RX_THRESH_CTRL | OPT_SECOND_FRAME | START_STOP_RX |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | Reset |

DIS_DROP_TCPPIP_ERR_FRAM Configures whether to disable dropping of TCP/IP checksum error frames.
O: Enable
1: Disable

When FWD_ERR_FRAME is O, this bit is ignored and all error frames are dropped. (R/W)

DIS_FLUSH_RECV_FRAMES Configures whether to disable flushing of received frames because of the unavailability of receive descriptors or buffers.
O: Enable
1: Disable
(R/W)

FLUSH_TX_FIFO Configures whether to flush TX FIFO to default values.
O: Not flush
1: Flush
(R/WS/SC)

TX_THRESH_CTRL Configures the threshold of TX FIFO. Transmission starts when the frame size within the TX FIFO is larger than the threshold. In addition, full frames with a length less than the threshold are also transmitted.

0: 64
1: 128
2: 192
3: 256
4: 40
5: 32
6: 24
7: 16

Transmission starts when the frame size within the TX FIFO is larger than the threshold. In addition, full frames with a length less than the threshold are also transmitted.
(R/W)

Continued on the next page...
```