**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Table of Bits and Names with Descriptions**

- **[27] DC: Disable CRC**
  - Description: When this bit is set, the MAC does not append a cyclic redundancy check (CRC) to the end of the transmitted frame. This is valid only when the first segment (TDESO[28]) is set.

- **[26] DP: Disable Pad**
  - Description: When set, the MAC automatically adds padding and CRC to a frame shorter than 64 bytes; this bit resets it.
  
- **[25] Reserved**
  - Description: Reserved

- **CRCR: CRC Replacement Control**
  - Description:
    - When set, the MAC replaces the last four bytes of the transmitted packet with recalculated CRC bytes. The host should ensure that the CRC bytes are present in the frame being transmitted from the Transmit Buffer.
    - This bit is valid when the First Segment control bit (TDESO[28]) is set.

- **CIC: Checksum Insertion Control**
  - Description:
    - These bits control the checksum calculation and insertion. The following list describes the bit encoding:

      - `2'b00`: Checksum insertion is disabled.
      - `2'b01`: Only IP header checksum calculation and insertion are enabled.

- **[23:22]**
  - Description:
    - `2'b10`: IP header checksum and payload checksum calculation and insertion are enabled, but pseudo-header checksum is not calculated in hardware. This field is valid when the First Segment control bit (TDESO[28]) is set.

- **TER: Transmit End of Ring**
  - Description:

      - When set, this bit indicates that the descriptor list reached its final descriptor.
      - The DMA returns to the base address of the list creating a Descriptor Ring. This should be set to `1`.

- **TCH: Second Address Chained**
  - Description:
    - When set, it indicates that the second address in the descriptor is the Next Descriptor address rather than the second buffer address.
    - TDESO[20] takes precedence over TDESO[20]. This bit should be set to `1`.

**Footer:**
Espressif Systems
476 ESP32 TRM (Version 5.6)
Submit Documentation Feedback