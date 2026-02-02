**Chapter 24: Ethernet Media Access Controller (EMAC)**

---

### Bits | Name | Description
---|---|---
[19:18] | VLIC: VLAN Insertion Control | When set, these bits request the MAC to perform VLAN tagging or untagging before transmitting the frames. If the frame is modified for VLAN tags, the MAC automatically recalculates and replaces the CRC bytes. The following list describes the values of these bits:
- 2^b00: Do not add a VLAN tag.
- 2^b01: Remove the VLAN tag from the frames before transmission. This option should be used only with the VLAN frames.

[19] | Reserved | Insert a VLAN tag with the tag value programmed in VLAN Tag Inclusion or Replacement Register.

[17] | Reserved | Replace the VLAN tag in frames with the Tag value programmed in VLAN Tag Inclusion or Replacement Register. This option should be used only with the VLAN frames.
- When set, this bit indicates that the MAC transmitter detected an error in the IP datagram header. The transmitter checks the header length in the IPv4 packet against the number of header bytes received from the application and indicates an error status if there is a mismatch.

[16] | IHE: IP Header Error | For IPv6 frames, a header error is reported when the main header length is not 40 bytes. Furthermore, the Ether-net Length/Type field value for an IPv4 or IPv6 frame must match the IP header version received with the packet.
- For IPv4 frames, an error status is also indicated if the Header Length field has a value less than 0x5.

[15] | ES: Error Summary | Indicates the logical OR of the following bits:
- TDES0[14]: Jabber Timeout
- TDES0[13]: Frame Flush
- TDES0[11]: Loss of Carrier
- TDES0[10]: No Carrier
- TDES0[9]: Late Collision
- TDES0[8]: Excessive Collision
- TDES0[2]: Excessive Deferral
- TDES0[1]: Underflow Error

[14] | JT: Jabber Timeout | When set, this bit indicates the MAC transmitter has experienced a jabber timeout. This bit is only set when EMACCONFIG_REG’s bit EMACJABBER is not set.

[13] | FF: Frame Flushed | When set, this bit indicates that the DMA or MTL flushed the frame because of a software Flush command given by the CPU.
- IP Header Error
- IP Payload Error

---

**Espressif Systems**
477 ESP32 TRM (Version 5.6)

Submit Documentation Feedback