

```markdown
Register 52.8. DMAIN_EN_REG (0x101C)

DMAIN_NISE Write 1 to enable and write 0 to disable the summary of the following normal interrupt enable bits:
Bit[0]: Transmit Interrupt
Bit[2]: Transmit Buffer Unavailable
Bit[6]: Receive Interrupt
Bit[14]: Early Receive Interrupt
(R/W)

DMAIN_AISE Write 1 to enable and write 0 to disable the summary of the following abnormal interrupt enable bis:
Bit[1]: Transmit Process Stopped
Bit[3]: Transmit Jabber Timeout
Bit[4]: Receive FIFO Overflow
Bit[5]: Transmit Underflow
Bit[7]: Receive Buffer Unavailable
Bit[8]: Receive Process Stopped
Bit[9]: Receive Watchdog Timeout
Bit[10]: Early Transmit Interrupt
Bit[13]: Fatal Bus Error
(R/W)

DMAIN_ERIE Write 1 to enable and write 0 to disable EARLY_RECV_INT. (R/W)

DMAIN_FBEE Write 1 to enable and write 0 to disable FATAL_BUS_ERR_INT.(R/W)

DMAIN_ETIE Write 1 to enable and write 0 to disable EARLY_TRANSS_INT. (R/W)

DMAIN_RWTE Write 1 to enable and write 0 to disable RECV_WDT_TO_INT. (R/W)

DMAIN_RSE Write 1 to enable and write 0 to disable RECV_PROC_STOP_INT. (R/W)

DMAIN_RBUE Write 1 to enable and write 0 to disable RECV_BUF_UNAVAIL_INT. (R/W)

DMAIN_RIE Write 1 to enable and write 0 to disable RECV_INT. (R/W)
```
Continued on the next page...
```