**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Heading:**
GoBack

**Table Descriptions and Content:**

1. **Table Description:** Table 27.8-2, DES1  
   - Bits | Name | Description  
   - --- | --- | ---  
   - 31:26 | Reserved | Reserved  
   - 25:13 | Reserved | Reserved  
   - 12:0 | BS1 (Buffer 1 Size) | Indicates the data buffer byte size, which must be a multiple of four. In the case where the buffer size is not a multiple of four, the resulting behavior is undefined. This field should not be zero.

2. **Table Description:** Table 27.8-3, DES2  
   - Bits | Name | Description  
   - --- | --- | ---  
   - 31:0 | Buffer Address Pointer 1 | These bits indicate the physical address of the data buffer.

3. **Table Description:** Table 27.8-4, DES3  
   - Bits | Name | Description  
   - --- | --- | ---  
   - 31:0 | Next Descriptor Address | If the Second Address Chained (DES0[4]) bit is set, then this address contains the pointer to the physical memory where the Next Descriptor is present. If this is not the last descriptor, then the Next Descriptor address pointer must be DES3[1:0] = 0.

**Subsection Heading and Content:**  
27.9 Initialization

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)