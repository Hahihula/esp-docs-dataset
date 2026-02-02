**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Diagram Description and Table:**

- **Figure Caption:** Figure 24.8-2. Receive Descriptor

- **Table Header:** Table 24.8-5. Receive Descriptor 0 (RDES0)
  
  | Bits | Name          | Description                                                                                   |
  |------|--------------|-----------------------------------------------------------------------------------------------|
  | [31] | OWN: Own Bit | When set, this bit indicates that the descriptor is owned by the DMA of the DWC_gmac. When this bit is reset, it indicates that the descriptor is owned by the Host. The DMA clears this bit either when it completes the frame reception or when the buffers that are associated with this descriptor are full. |
  | [30] | AFM: Destination Address Filter Fail | When set, this bit indicates a frame failed in the DA Filter in the MAC. These bits indicate the byte length of the received frame that was transmitted to host memory. This field is valid when Last Descriptor (RDES0[8]) is set and either the Descriptor Error (RDESQ[14]) or Overflow Error bits are reset. The frame length also includes two bytes appended to the Ethernet frame when IP checksum calculation (Type 1) is enabled and the received frame is not a MAC control frame. Indicates the logical OR of the following bits: |
  | [29:16]| FL: Frame Length | This field indicates only when the Last Descriptor (RDES0[8]) is set. |
  | [15] | ES: Error Summary | When set, this bit indicates a frame truncation caused by a frame that does not fit within the current descriptor buffers, and that the DMA does not own the Next Descriptor. The frame is truncated. This field is valid only when the Last Descriptor (RDES0[8]) is set. |
  | [14] | DE: Descriptor Error | |

**Text Explanation for Table Entries:** 

- **OWN**: Own Bit
  - When this bit indicates that the descriptor is owned by the DMA of the DWC_gmac.
  - When it's reset, it means the descriptor is owned by the Host. The DMA clears this bit either when completing frame reception or upon buffer association with this descriptor.

- **AFM: Destination Address Filter Fail**
  - Indicates a failed DA filter in MAC for received frames and their byte length transmitted to host memory.
  - Valid conditions include Last Descriptor (RDES0[8]) being set, and either Descriptor Error (RDESQ[14]) or Overflow Error bits reset.

- **FL: Frame Length**
  - This field is valid only when the Last Descriptor (RDES0[8]) is set. 

- **ES: Error Summary**
  - Indicates a frame truncation due to an oversized fit within current descriptor buffers.
  - DMA does not own Next Descriptor, and this condition occurs if RDES0[8] is set.

**Footer Information:** 
Espressif Systems
480 ESP32 TRM (Version 5.6)
Submit Documentation Feedback