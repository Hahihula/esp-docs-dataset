**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Table of Contents for Table Descriptions and Details**

1. **Table Description:** Word DES1 of SD/MMC GDMA Linked List

   - Bits | Name | Description
   - --- | --- | ---
   - 31:26 | Reserved | Reserved
   - 25:13 | Reserved | Reserved
   - 12:0 | BS (Buffer Size) | Indicates the size of the data buffer (in Byte), which must be a multiple of four. In the case where the buffer size is not a multiple of four, the resulting behavior is undefined. This field should not be zero.

2. **Table Description:** Word DES2 of SD/MMC GDMA Linked List

   - Bits | Name | Description
   - --- | --- | ---
   - 31:0 | Buffer Address Pointer | These bits indicate the physical address of the data buffer. And the buffer address must be word-aligned.

**Text Content and Descriptions for Each Bit Field in DES1 Element**

- **CH (Second Address Chained)**
  - Bits Position: 4
  - Description:
    When set, this bit indicates that the second address in the descriptor is the Next Descriptor address. This means when it's set to BS2 (DES1[25:13]), all bits should be zeros.

- **FD (First Descriptor)**
  - Bits Position: 3
  - Description:
    When set, this bit indicates that this descriptor contains the first buffer of data. If the size of the first buffer is zero, then Next Descriptor will contain a beginninging of the data transfer.
  
- **LD (Last Descriptor)**
  - Bits Position: 2
  - Description:
    This bit associates with last block of DMA transfer when set this indicates that buffers pointed by this descriptor are Last Buffers. After this descriptor is completed, remaining byte count should be zero.

- **DIC (Disable Interrupt on Completion)**
  - Bits Position: 1
  - Description:
    When set, it prevents the setting of TI/RI bit in DMA Status Register (IDSTS) for data that ends buffer pointed by this descriptor.
  
- **Reserved**
  - Bits Positions: All other bits from position to zero are reserved.

**Text Content and Descriptions for Each Bit Field in DES2 Element**

The DES2 element contains the address pointer of a data buffer. 

**Text Content and Descriptions for Each Bit Field in DES3 Element**

The DES3 element has an address pointer that points next descriptor if present descriptor is not last one in chained descriptor structure.

**Footer Information:**
- Company Name: Espressif Systems
- Document Version: ESP32-S3 TRM (Version 1.7)
- Page Number and Feedback Link:
  - "Submit Documentation Feedback" at the bottom of each page.
  
**Navigation Links:** 
- GoBack button is available for navigation to previous sections or chapters.

This structured description should help in understanding all textual content from this document without needing direct visual access, especially useful when dealing with complex technical documents.