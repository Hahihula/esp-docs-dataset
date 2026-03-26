

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC) GoBack

Register 52.6. DMASTATUS_REG (0x1014)

Continued from the previous page...

NORM_INT_SUMM Represents the logical OR of the following when the corresponding interrupt bits are enabled in Interrupt Enable Register.
Bit[0]: Transmit Interrupt
Bit[2]: Transmit Buffer Unavailable
Bit[6]: Receive Interrupt
Bit[14]: Early Receive Interrupt
Only unmasked interrupts affect this bit.
This is a sticky bit and must be cleared (by writing 1 to this bit) each time a corresponding bit, which causes this set to be set, is cleared. (R/SS/WC)

ABN_INT_SUMM Represents the logical OR of the following when the corresponding interrupt bits are enabled in Interrupt Enable Register.
Bit[1]: Transmit Process Stopped
Bit[3]: Transmit Jabber Timeout
Bit[4]: Receive FIFO Overflow
Bit[5]: Transmit Underflow
Bit[7]: Receive Buffer Unavailable
Bit[8]: Receive Process Stopped
Bit[9]: Receive Watchdog Timeout
Bit[10]: Early Transmit Interrupt
Bit[13]: Fatal Bus Error
Only unmasked interrupts affect this bit.
This is a sticky bit and must be cleared each time a corresponding bit, which causes this bit to be set, is cleared. (R/SS/WC)

EARLY_RECV_INT The raw interrupt status of EARLY_RECV_INT.(R/SS/WC)

FATAL_BUS_ERR_INT The raw interrupt status of FATAL_BUS_ERR_INT. (R/SS/WC)

EARLY_TRAN_INT The raw interrupt status of EARLY_TRAN_INT. (R/SS/WC)

RECV_WDT_TO Represents whether the Receive Watchdog Timer expired while receiving the current frame and the current frame is truncated after the watchdog timeout.
0: Not expired
1: Expired
(R/SS/WC)

RECV_PROC_STOP Represents whether the Receive Process enters the Stopped state.
0: Not stopped
1: Stopped
(R/SS/WC)

Continued on the next page...
```