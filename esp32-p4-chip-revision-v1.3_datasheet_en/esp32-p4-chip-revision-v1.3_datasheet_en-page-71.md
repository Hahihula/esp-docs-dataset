**4 Functional Description**

- Automatic CRC and padding (all O) generation controllable on a per-frame basis

- Options for automatic padding generation for data below the minimum frame length

- Programmable frame length supporting jumbo frames of up to 16 KB

- Programmable inter-frame gap (IFG) from 40 to 96 bit times in steps of 8

**Flexible address filtering modes:**
   - Up to eight 48-bit perfect address filters with per-byte masking
   - Up to eight 48-bit source address (SA) comparisons with per-byte masking
   - Option to pass all multicast addressed frames
   - Promiscuous mode to pass all frames without filtering for network monitoring

- Passes all incoming packets (as per filter) with a status report

- Separate 32-bit status returned for transmission and reception packets

- IEEE 802.1Q VLAN tag detection for reception frames

- Separate transmission, reception, and control interfaces for the application

- Management Data Input/Output (MDIO) interface for PHY device configuration and management

- Checksum offload for received IPv4 and TCP packets encapsulated by the Ethernet frame

- Checking IPv4 header checksum and TCP, UDP, or ICMP checksum encapsulated in IPv4 or IPv6 datagrams

- 64-bit timestamp for each transmitted and received frame (see IEEE 1588-2008)

- Energy Efficient Ethernet support (see IEEE 802.3az-2010)

- CRC replacement, SA insertion/replacement, and VLAN insertion/removal/deletion in transmit frames

- Two FIFOs: 256-byte TX FIFO and 256-byte RX FIFO

- Receive status vectors inserted into RX FIFO after the EOF (end of frame) transfer, allowing multiple-frame storage without requiring an additional FIFO for status

- Option to forward good run frames

- Statistics generation with pulse signaling for dropped or corrupted frames due to RX FIFO overflow

- Automatic re-transmission of collision frames

- Frame discarding in cases of late collisions, excessive collisions, excessive deferrals, or underflow conditions

- Software control for TX FIFO flushing

**Pin Assignment**

The Ethernet media access controller includes only one RMII interface. For flexible pin routing, each RMII signal offers three alternative GPIO mappings:

- RMII Group 1: Signals are multiplexed with GPIO28-GPIO36 and the SPI2 interface via IO MUX.

Espressif Systems

71
Submit Documentation Feedback