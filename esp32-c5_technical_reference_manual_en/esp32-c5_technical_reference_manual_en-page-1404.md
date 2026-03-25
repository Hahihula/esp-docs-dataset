

```markdown
Chapter 38 Controller Area Network Flexible Data-Rate (CAN FD) GoBack

Register 38.2. TWAIFD_MODE_SETTINGS_REG (0x0004)

Continued from the previous page...

TWAIFD_TSTM Configures whether to enable the test mode.
O: Disable
1: Enable
(R/W)

TWAIFD_RXBAM Configures whether to enable the RX buffer automatic mode.
O: Disable
1: Enable
(R/W)

TWAIFD_TXBBM Configures whether to enable the TX buffer backup mode.
O: Disable
1: Enable
(R/W)

TWAIFD_SAM Configures whether to enable the self acknowledge mode.
O: Disable
1: Enable
(R/W)

TWAIFD_RTRLE Configures whether to enable the retransmission limitation.
O: Disable
1: Enable
(R/W)

TWAIFD_RTRTH Configures the retransmission limit. Maximal amount of retransmission attempts when TWAIFD_RTRLE is enabled. (R/W)

TWAIFD_ILBP Configures whether to enable the loopback mode.
O: Disable
1: Enable
(R/W)

TWAIFD_ENA Configures whether to enable CAN FD.
O: Disable
1: Enable
(R/W)

TWAIFD_NISOFD Configures whether CAN FD conforms to ISO protocols. Modify only when TWAIFD_ENA = 0.
O: Conform to ISO
1: Conform to CAN FD 1.0, not ISO
(R/W)

Continued on the next page...
```