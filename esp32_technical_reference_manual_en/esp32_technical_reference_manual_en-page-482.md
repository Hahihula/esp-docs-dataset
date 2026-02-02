**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Table of Bits and Names with Descriptions**

1. **CE: CRC Error**
   - Description:
     When set, this bit indicates that a Cyclic Redundancy Check (CRC) Error occurred on the received frame. This field is valid only when the Last Descriptor (RDES0[8]) is set.

2. **Extended Status Available/ Rx MAC Address [0]**
   - Description:
     When the IP Checksum Offload (Type 2) is present, this bit indicates that the extended status word available in descriptor RDES4(3). This field can be valid only when Last Descriptor bit (RDES0[8]) is set. It becomes invalid if Bit 30 of the descriptor header is not zero.

   - When IP Checksum Offload (Type 2) is present, this bit indicates that even without an IP Checksum Offload engine bypasses processing for non-IP frames or IP frames with a non-TCP/UDP/ICMP payload.
   
     If IPC Full Offload does not exist in the descriptor header:
     - This field can indicate whether Rx MAC Address registers value (1 to 15) matched frame's DA field.

3. **Receive Descriptor 1 (RDES1)**

   | Bits | Name       | Description                                                                                   |
   |------|------------|------------------------------------------------------------------------------------------------|
   | [31] | Ctrl       | When set, this bit prevents setting the Status Register’s RI bit for received frames that end in buffer indicated by this descriptor. This action disables assertion of interrupt to Host because RIs are reserved for that frame. |
   
   - Reserved
     - Reserved
   
   | Bits | Name       | Description                                                                                   |
   |------|------------|------------------------------------------------------------------------------------------------|
   | [15] | RER: Receive End of Ring                          | When set, this bit indicates the descriptor list reached its final descriptor. The DMA returns to base address of the list for creating Descriptor Ring. |
   
   - Reserved
     - Reserved
   
   | Bits | Name       | Description                                                                                   |
   |------|------------|------------------------------------------------------------------------------------------------|
   | [14] | RCH: Second Address Chained                       | When set, this bit indicates that second descriptor in the descriptor is Next Descriptor address rather than buffer. This field takes precedence over RDES[15]. |
   
   - Reserved
     - Reserved
   
   | Bits | Name       | Description                                                                                   |
   |------|------------|------------------------------------------------------------------------------------------------|
   | [13] | Reserved   | Indicates first data buffer size in bytes. Buffer must be multiple of 4, even if the value RDES2 (buffer1 address pointer) is not aligned to bus width. When buffer size does not align with a factor of four, resulting behavior undefined. If this field equals zero, DMA ignores that buffer and uses next descriptor depending on bit [RCH(14)]. |
   
   | Bits | Name       | Description                                                                                   |
   |------|------------|------------------------------------------------------------------------------------------------|
   | [12:0]| RBS1: Receive Buffer 1 Size                      | Indicates the first data buffer size in bytes. The buffer must be multiple of four, even if value is not aligned to bus width. |

**Footer Information**
- Page Number: 482
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

**Navigation Links:** 
- Submit Documentation Feedback