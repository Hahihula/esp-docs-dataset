

```markdown
Chapter 38 Controller Area Network Flexible Data-Rate (CAN FD)    GoBack


Register 38.2. TWAIFD_MODE_SETTINGS_REG (0x0004)


Continued from the previous page...


TWAIFD_PEX   Configures whether to enable protocol exception handling. Modify only when
             TWAIFD_ENA = 0.
O: Disable
1: Enable
(R/W)

TWAIFD_TBFBO   Configures whether all TX buffers enter "TX failed" state when CAN FD becomes bus-off.
O: Not enter "TX failed"
1: Enter "TX failed"
(R/W)

TWAIFD_FDRF   Configures whether frame filters drop RTR frames.
O: Accept
1: Drop
(R/W)

TWAIFD_PCHKE   Configures whether to enable parity checks in TX buffers and RX buffer.
O: Disable
1: Enable
(R/W)
```