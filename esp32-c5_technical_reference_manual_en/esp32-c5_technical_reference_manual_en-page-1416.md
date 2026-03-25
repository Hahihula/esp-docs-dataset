

```markdown
Register 38.18. TWAIFD_STATUS_REG (0x0008)

Continued from the previous page...

TWAIFD_PEXS Represents whether a protocol exception occurs.
O: Not occur
1: Occur; can be cleared by writing 1 to TWAIFD_CPEXS
(RO)

TWAIFD_RXPE Represents whether a parity error is detected during the read of a CAN frame from the RX buffer via TWAIFD_RX_DATA.
O: Not detected
1: Detected
(RO)

TWAIFD_TXPE Represents whether a parity error is detected in a TX buffer during transmission from that buffer
O: Not detected
1: Detected
(RO)

TWAIFD_TXDPE Represents whether a double parity error is detected in the "backup" TX buffer while in TX buffer backup mode.
O: Not detected
1: Detected
(RO)

TWAIFD_STCNT Represents whether to enable traffic counters.
O: Disable
1: Enable
(RO)

TWAIFD_STRGS Represents whether to enable test registers for memory testability.
O: Disable
1: Enable
(RO)
```