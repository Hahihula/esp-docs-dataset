**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Table of Bits and Names with Descriptions**

| Bits | Name                          | Description                                                                                   |
|------|-------------------------------|------------------------------------------------------------------------------------------------|
| [6]  | IPv4 Packet Received          | When set, this bit indicates that the received packet is an IPv4 packet. This bit is updated only when Bit[10] (IPC) of Register (MAC Configuration Register) is set. |
| [5]  | IP Checksum Bypassed         | When set, this bit indicates that the checksum offload engine is bypassed.                   |
| [4]  | IP Payload Error             | When set, this bit indicates that the 16-bit IP payload checksum (that is, the TCP, UDP, or ICMP checksum) that the core calculated does not match the corresponding checksum field in the received segment. It is also set when the TCP, UDP, or ICMP segment length does not match the payload length value in the IP Header field. This bit is valid when either Bit 7 or Bit 6 is set. |
| [3]  | IP Header Error              | When set, this bit indicates that either the 16-bit IPv4 header checksum calculated by the core does not match the received checksum bits of bytes, or the IP datagram version is not consistent with the Ethernet Type value. This bit is valid when either Bit[7] or Bit[6] is set. |
| [2:0]| IP Payload Type              | These bits indicate the type of payload encapsulated in the IP datagram processed by the Receive Checksum Offload Engine (COE). The COE also sets these bits to 2'b00 if it does not process the IP datagram's payload due to an IP header error or fragmented IP. This bit is valid when either Bit[7] or Bit[6] is set. |

**Section Title:**
24.9 Register Summary

**List of Attributes for Registers**

- Read Only (RO)
- Write Only (WO)
- Read and Write (R/W)
- Read, Write, and Self Clear (R/W/SC)
- Read, Set, and Write Clear (R/SS/WC)
- Read, Write Set, and Self Clear (R/WS/SC)
- Read, Self Set, and Self Clear or Write Clear (R/SS/SC/WC)
- Read Only and Write Trigger (RO/WT)

**Footer:**
Espressif Systems
484 ESP32 TRM (Version 5.6) Submit Documentation Feedback