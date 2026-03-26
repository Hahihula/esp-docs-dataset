

```markdown
Register 52.16. EMACCONFIG_REG (0x0000)

Continued from the previous page...

EMACJUMBOFRAME Configures whether the MAC allows Jumbo frames of 9,018 bytes (9,022 bytes for VLAN tagged frames) without reporting a giant frame error in the receive frame status.
O: Not allow
1: Allow
(R/W)

EMACINTERFRAMEGAP Configures the minimum interframe gap (IFG) between frames during transmission.
O: 96 bit times
1: 88 bit times
2: 80 bit times
3: 72 bit times
4: 64 bit times
5: 56 bit times
6: 48 bit times
7: 40 bit times

In the half-duplex mode, the minimum IFG can be configured only for 64 bit times (IFG = 100).
(R/W)

EMACDISABLECRS Configures whether to disable Carrier Sense during transmission.
O: The MAC transmitter generates Loss of Carrier or No Carrier errors because of Carrier Sense and can even abort the transmissions.
1: The MAC transmitter ignores the MII CRS signal during frame transmission in the half-duplex mode. This request results in no errors generated because of Loss of Carrier or No Carrier during such transmission.
(R/W)

EMACMII Configures the Ethernet line speed.
O: For 1000 Mbps operations
1: For 10 or 100 Mbps operations

In 10 or 100 Mbps operations, the exact line speed is determined by both this bit and the FES (EMACFESPEED) bit. (R/W)

EMACFESPEED Configures the speed in the MII and RMII interface.
O: 10 Mbps
1: 100 Mbps
(R/W)

EMACRXOWN Configures whether to disable receive own.
O: The MAC receives all packets that are given by the PHY while transmitting.
1: the MAC disables the reception of frames when TX_EN triggers an interrupt in the half-duplex mode.

This bit is not applicable if the MAC is operating in the full-duplex mode. (R/W)

Continued on the next page...
```