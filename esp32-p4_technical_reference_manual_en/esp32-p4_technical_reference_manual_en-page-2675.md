

```markdown
Register 52.50. EMACTSTPCTRL_REG (0x0700)
```

Continued from the previous page...

TSIPV6ENA Configures whether to enable the processing of PTP frames sent over IPv6-UDP.
0: Disable. The MAC ignores the PTP transported over UDP-IPv6 packets
1: Enable. The MAC receiver processes the PTP packets encapsulated in UDP over IPv6 packets (R/W)

TSIPENA Configures whether to enable the processing of PTP sent over Ethernet frames.
0: Disable. the MAC ignores the PTP over Ethernet packets
1: Enable. The MAC receiver processes the PTP packets encapsulated directly in the Ethernet frames (R/W)

TSVER2ENA Configures whether to enable PTP packet processing for version 2 format.
0: Disable. The PTP packets are processed using the version 1 format
1: Enable. The PTP packets are processed using the 1588 version 2 format (R/W)

TSCTRLSSR Configures the timeout digital or binary rollover.
0: The Timestamp Low register rolls over after the value of the sub-second register 0x7FFF_FFFF. The sub-second increment has to be programmed correctly depending on the PTP reference clock frequency and the value of this bit.
1: The Timestamp Low register rolls over after 0x3B9A_C9FF value (that is, 1 nanosecond accuracy) and increments the timestamp (High) seconds. (R/W)

TSENALL Configures whether to enable timestamp for all frames received by the MAC.
0: Disable
1: Enable (R/W)

TSADDREG Configures whether to update the content of the EMACTSTPADEND_REG register in the PTP block for fine correction.
0: Not update
1: Update
This bit should be zero before setting it. (R/WS/SC)

Continued on the next page...
```