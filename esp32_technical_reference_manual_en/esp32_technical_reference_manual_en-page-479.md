**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Tables and Descriptions**

- **Table 24.8-2. Transmit Descriptor 1 (TDES1)**
  - Bits | Name | Description
  - [31:29] | SAIC: SA Insertion Control | These bits request the MAC to add or replace the Source Address field in the Ethernet frame with the value given in the MAC Address O register. If the Source Address field is modified in a frame, the MAC automatically recalculates and replaces the CRC bytes. The Bit[31] specifies the MAC Address Register value (1 or 0) that is used for Source Address insertion or replacement. The following list describes the values of Bits[30:29]:
    - '2'b00: Do not include the source address.
    - '2'b01: Include or insert the source address. For reliable transmission, the application must provide frames without source addresses.
    - '2'b10: Replace the source address. For reliable transmission, the application must provide frames with source addresses.

- **Table 24.8-3. Transmit Descriptor 2 (TDES2)**
  - Bits | Name
  - [28:16] | Reserved
  - [15:13] | Reserved

- **Table 24.8-4. Transmit Descriptor 3 (TDES3)**
  - Bits | Name | Description
  - [31:0] | Buffer 1 Address Pointer | These bits indicate the physical address of Buffer 1.
  - [31:0] | Next Descriptor Address | This address contains the pointer to the physical memory where the Next Descriptor is present.

**Section Title and Subtitle**

- **24.8.2 Receive Descriptors**
  The structure of the receiver linked lists is shown in Figure 24.8-2. Table 24.8-5 to Table 24.8-9 provide the description of the linked lists.
  
**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Reference Number:** 
ESP32 TRM (Version 5.6)