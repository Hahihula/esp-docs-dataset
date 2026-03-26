

```markdown
- Carrier Sense Multiple Access or Collision Detection (CSMA/CD) protocol in half-duplex mode
- IEEE 802.3x flow control in full-duplex mode
- Optional forwarding of received pause control frame to the user application in full-duplex mode
- Back-pressure flow control in half-duplex mode
- Automatic transmission of zero-quanta pause frame on deassertion of flow control input in full-duplex mode

• Preamble and start-of-frame data (SFD) insertion in Transmit, and deletion in Receive paths
• Automatic CRC and padding (all 0) generation controllable on a per-frame basis
• Options for automatic padding generation for data below the minimum frame length
• Programmable frame length supporting jumbo frames of up to 16 KB
• Programmable inter-frame gap (IFG) from 40 to 96 bit times in steps of 8)

• Supports a variety of flexible address filtering modes:
    - Up to eight 48-bit perfect address filters with masks for each byte
    - Up to eight 48-bit source address (SA) address comparison check with masks for each byte
    - Option to pass all multicast addressed frames
    - Promiscuous mode support to pass all frames without any filtering for network monitoring
    - Passes all incoming packets (as per filter) with a status report

• Separate 32-bit status returned for transmission and reception packets
• Supports IEEE 802.1Q VLAN tag detection for reception frames
• Separate transmission, reception, and control interfaces for the application
• Management Data Input/Output (MDIO) interface for PHY device configuration and management
• Supports checksum off-load for received IPv4 and TCP packets encapsulated by the Ethernet frame
• Supports checking IPv4 header checksum and TCP, UDP, or ICMP checksum encapsulated in IPv4 or IPv6 datagrams
• Supports 64-bit timestamp on each transmit and receive frame (see IEEE 1588-2008)
• Supports Energy Efficient Ethernet (see IEEE 802.3az-2010)
• CRC replacement, SA insertion or replacement, and VLAN insertion, replacement or deletion in transmit frames
• Two FIFOs: 256-byte TX FIFO and 256-byte RX FIFO
• Receive status vectors inserted into RX FIFO after the EOF (end of frame) transfer, which enables multiple-frame storage in RX FIFO without requiring another FIFO to store those frames’ receive status
• Option to forward good run frames
• Supports statistics by generating pulses for frames dropped or corrupted due to overflow in RX FIFO
• Automatic re-transmission of collision frames (subject to certain conditions, see Section 52.4.1.1)
```