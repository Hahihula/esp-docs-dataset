**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Tables and Descriptions**

- **Table 24.8-7. Receive Descriptor 2 (RDES2)**
  - Bits [31:0]: Buffer 1 Address Pointer  
    Description: These bits indicate the physical address of Buffer 1.

- **Table 24.8-8. Receive Descriptor 3 (RDES3)**
  - Bits [31:0]: Next Descriptor Address
    Description: This address contains the pointer to the physical memory where the next descriptor is present.

- **Table 24.8-9. Receive Descriptor 4 (RDES4)**
  - Bits and Names with Descriptions:
    - [31:28]: Reserved
    - [27:26]: Reserved
    - [25]: Reserved
    - [24]: Reserved
    - [23:21]: Reserved
    - [20:18]: Reserved
    - [17]: Reserved
    - [16]: Reserved
    - [15]: Reserved
    - [14]: Reserved
    - [13]: Reserved
    - [12]: Reserved

      These bits are encoded to give the type of the message received.
      - 3'b0000: Reserved
      - 3'b0001: SYNC (all clock types)
      - 3'b0010: Follow_Up (all clock types)
      - 3'b0011: Delay_Req (all clock types)
      - 3'b0100: Delay_Resp (all clock types)
      - 3'b0101: Pdelay_Req (in peer-to-peer transparent clock)
      - 3'b0110: Pdelay_Resp (in peer-to-peer transparent clock)
      - 3'b0111: Pdelay_Resp_Follow_Up (in peer-to-peer transparent clock)

    - [11:8]: Message Type
      - 3'b1000: Announce
      - 3'b1001: Management
      - 3'b1010: Signaling

    - [7]: IPv6 Packet Received packet.
      When set, this bit indicates that the received packet is an IPv6 packet. This bit is updated only when Bit[10] (IPC) of Register (MAC Configuration Register) is set.

**Footer Information**
- Espressif Systems
- Page Number: 483
- Document Version: ESP32 TRM (Version 5.6)
- Submit Documentation Feedback