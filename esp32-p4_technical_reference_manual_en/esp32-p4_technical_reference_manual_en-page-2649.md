

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC) GoBack


Register 52.16. EMACCONFIG_REG (0x0000)


Continued from the previous page...


EMACLOOPBACK Configures whether to enable the loopback mode.
O: Disable.
1: Enable. In this case, the MII Receive clock input (CLK_RX) is required for the loopback to work properly, because the Transmit clock is not looped-back internally.
(R/W)


EMACDUPLEX Configures whether to enable full-duplex mode, so that the MAC can transmit and receive simultaneously.
O: Disable
1: Enable
This bit is RO with a default value of 1 in the full-duplex-only configuration. (R/W)


EMACRXIPCOFFLOAD Configures whether to enable the checksum offload function
O: Disable
1: Enable
When the checksum offload function is enabled, the MAC calculates the 16-bit one's complement of the one's complement sum of all received Ethernet frame payloads. It also checks whether the IPv4 Header checksum (assumed to be bytes 25/26 or 29/30 (VLAN-tagged) of the received Ethernet frame) is correct for the received frame and gives the status in the receive status word. The MAC also appends the 16-bit checksum calculated for the IP header datagram payload (bytes after the IPv4 header) and appends it to the Ethernet frame transferred to the application (when Type 2 COE is deselected). (R/W)


EMACRETRY Configures whether to disable retry, so that the MAC attempts only one transmission, and when a collision occurs on the MII interface the MAC ignores the current frame transmission and reports a Frame Abort with excessive collision error in the transmit frame status.
O: Enable
1: Disable
Valid only in the half-duplex mode. (R/W)


EMACPADCRCSTRIP Configures whether to enable automatic Pad or CRC stripping.
O: Disable. In this case, the MAC passes all incoming frames, without modifying them, to the Host.
1: Enable. In this case, the MAC strips the Pad or FCS field on the incoming frames only if the value of the length field is less than 1,536 bytes. All received frames with length field greater than or equal to 1,536 bytes are passed to the application without stripping the Pad or FCS field.
(R/W)


Continued on the next page...
```