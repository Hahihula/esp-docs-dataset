**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Body Text:**

- If the flow control input signal disappears during a full-duplex operation, a pause frame with zero pause time value is automatically transmitted.
  
- The Preamble and the Start Frame Delimiter (SFD) are inserted in the Transmit path, and deleted in the Receive path.

- Cyclic Redundancy Check (CRC) and Pad can be controlled on a per-frame basis.

- The Pad is generated automatically, if data is below the minimum frame length.
  
- Programmable frame length supporting jumbo frames of up to 16 KB
  
- Programmable Inter-frame Gap (IFG) (40-96 bit times in steps of 8)
  
- Support for a variety of flexible address filtering modes:
  - Up to eight 48-bit perfect address filters to mask each byte
  - Up to eight 48-bit SA address comparison checks to mask each byte
  
  - All multicast address frames can be transmitted
  
  - All frames in mixed mode can be transmitted without being filtered for network monitoring
  
  - A status report is attached each time all incoming packets are transmitted and filtered

- Returning a 32-bit status for transmission and reception of packets respectively
  
- Separate transmission, reception, and control interfaces for the application
  
- Use of the Management Data Input/Output (MDIO) interface to configure and manage PHY devices
  
- Support for the offloading of received IPv4 and TCP packets encapsulated by an Ethernet frame in the reception function
  
- Support for checking IPv4 header checksums, as well as TCP, UDP, or ICMP (Internet Control Message Protocol) checksums encapsulated in IPv4/IPv6 packets in the enhanced reception function
  
- Two sets of FIFOs: one 2 KB Tx FIFO with programmable threshold and one 2 KB Rx FIFO with configurable threshold (64 bytes by default)
  
- When Rx FIFO stores multiple frames, the Receive Status Vector is inserted into the Rx FIFO after transmitting an EOF (end of frame), so that the Rx FIFO does not need to store the Receive Status of these frames
  
- In store-and-forward mode, all error frames can be filtered during reception, but not forwarded to the application.
  
- Under-sized good frames can be forwarded.
  
- Support for data statistics by generating pulses for lost or corrupted frames in the Rx FIFO due to an overflow
  
- Support for store-and-forward mechanism when transmitting data to the MAC core
  
- Automatic re-transmission of collided frames during transmission (subject to certain conditions, see section 24.2.1.2)
  
- Discarding frames in cases of late collisions, excessive collisions, excessive deferrals, and under-run conditions

**Footer:**
Espressif Systems
Submit Documentation Feedback
ESP32 TRM (Version 5.6)