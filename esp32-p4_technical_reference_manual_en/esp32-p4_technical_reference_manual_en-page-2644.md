

```markdown
Register 52.8. DMAIN_EN_REG (0x101C)

Continued from the previous page...

DMAIN_UIE Write 1 to enable and write 0 to disable TRANS_UNDFLOW_INT. (R/W)
DMAIN_OIE Write 1 to enable and write 0 to disable RECV_OVFLOW_INT. (R/W)
DMAIN_TJTE Write 1 to enable and write 0 to disable TRANS_JABBER_TO_INT. (R/W)
DMAIN_TBUE Write 1 to enable and write 0 to disable TRANS_BUF_UNAVAIL_INT. (R/W)
DMAIN_TSE Write 1 to enable and write 0 to disable TRANS_PROC_STOP_INT.(R/W)
DMAIN_TIE Write 1 to enable and write 0 to disable TRANS_INT.(R/W)

Register 52.9. DMAMISSEDFR_REG (0x1020)


| 31 | 29 | 28 | 27 | Overflow_BFOC | Overflow_FC | Overflow_BMFC | Missed_FC | 0 |
|----:|----:|----:|----:|--------------:|-------------:|---------------:|----------:|---|
|   0 |   0 | 0x0 | 0x0 |           0x0  |          0x0 |            0x0 |     0x0  | Reset |

Overflow_BFOC Represents the status of the overflow frame counter.
O: No overflow.

1: The overflow frame counter (Overflow_FC) overflows, that is, the RX FIFO overflows with the
overflow frame counter at maximum value. In such a scenario, the overflow frame counter is
reset to all-zeros.
(R/SS/RC)

Overflow_FC Represents the number of frames missed by the application.
This counter is incremented each time the MTL FIFO overflows. (R/SS/RC)

Overflow_BMFC Represents the status of the missed frame counter.
O: No overflow.

1: The missed frame counter (Missed_FC) overflows, that is, the Host Receive Buffer being
unavailable with the missed frame counter at maximum value. In such a scenario, the Missed
frame counter is reset to all-zeros.
(R/SS/RC)

Missed_FC Represents the number of frames missed by the controller because of the Host Receive
Buffer being unavailable.
This counter is incremented each time the DMA discards an incoming frame. (R/SS/RC)
```