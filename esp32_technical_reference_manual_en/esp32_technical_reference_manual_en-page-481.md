**Chapter 24: Ethernet Media Access Controller (EMAC)**

---

| Bits | Name                          | Description                                                                 |
|------|-------------------------------|-----------------------------------------------------------------------------|
| [13] | SAF: Source Address Filter    | When set, this bit indicates that the SA field of frame failed the SA Fail in the MAC. |
| [12] | LE: Length Error              | When set, this bit indicates that the actual length of the frame received and that the Length/Type field does not match. This bit is valid only when the Frame Type (RDESQ[5]) bit is reset. |
| [11] | OE: Overflow Error            | When set, this bit indicates that the received frame was damaged because of buffer overflow in MTL. |
| [10] | VLAN: VLAN Tag                | When set, this bit indicates that the frame to which this descriptor is pointing is a VLAN frame tagged by the MAC. The VLAN tagging depends on checking the VLAN fields of the received frame based on the Register (VLAN Tag Register) settings. |
| [9]  | FS: First Descriptor          | When set, this bit indicates that this descriptor contains the first buffer of the frame. If the size of the first buffer is O, the second buffer contains the beginning of the frame. If the size of the second buffer is also O, then the next Descriptor contains the beginning of the frame. |
| [8]  | LS: Last Descriptor            | When set, this bit indicates that the buffers pointed to by this descriptor are the last buffers of the frame. |
| [7]  | IP Checksum Error (Type1), or Giant Frame                           | If IP Checksum Engine (Type 1) is selected, this bit, if set, indicates one of the following: The 16-bit IPv4 header checksum calculated by the core did not match the received checksum bytes. The header checksum checking is bypassed for non-IPv4 frames. Otherwise, when set, it indicates that Giant Frame Status. Giant frames are larger than 1,518 bytes (or 1,522 bytes for VLAN or 2,000 bytes when Bit[27] of the MAC Configuration register is set), normal frames and larger-than-9,018-byte (9,022-byte for VLAN) frames when Jumbo Frame processing is enabled. |
| [6]  | LC: Late Collision            | When set, this bit indicates that a late collision has occurred while receiving the frame in half-duplex mode. |
| [5]  | FT: Frame Type                | When set, this bit indicates that the Receive Frame is an Ethernet-type frame (the LT field is greater than or equal to, 1,536). When this bit is reset, it indicates that received frame is an IEEE 802.3 frame. This bit is not valid for Runt frames which are less than 14 bytes. |
| [4]  | RWT: Receive Watchdog Timeout | When set, this bit indicates that the Receive Watchdog Timer has expired while receiving the current frame and the current frame is truncated after the Watchdog Timeout. |
| [3]  | RE: Receive Error             | When set, this bit indicates that the MII_RXER signal is asserted while MII_RXDV is asserted during frame reception. |
| [2]  | DE: Dribble Bit Error         | When set, this bit indicates that the received frame has a non-integer multiple of bytes (odd nibbles). This bit is valid only in the MII Mode.

---

**Footer:**  
Espressif Systems  
481 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback