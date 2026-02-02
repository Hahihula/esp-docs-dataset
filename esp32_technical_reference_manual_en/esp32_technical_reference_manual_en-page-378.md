**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Header and Register Information with Description:**

1. **Register Name:** SPI_SLV_WRBUF_DLEN_REG  
   **Address Offset:** 0x48

   - **Description:** 
     - **Field Label:** (reserved)
     - **Field Bits:** [31, 24, 23] to [0]
     - **Reset Value:** 0x00000000
     - **Functionality:**
       - **SPI_SLV_WRBUF_DBITLEN**: It indicates the length of written data minus one, in multiples of one bit.  
         *It is only valid in slave half-duplex mode.* (R/W)

2. **Register Name:** SPI_SLV_RDBUF_DLEN_REG
   **Address Offset:** 0x4C

   - **Description:**
     - **Field Label:** (reserved)
     - **Field Bits:** [31, 24, 23] to [0]
     - **Reset Value:** 0x00000000
     - **Functionality:**
       - **SPI_SLV_RDBUF_DBITLEN**: It indicates the length of read data minus one, in multiples of one bit.  
         *It is only valid in slave half-duplex mode.* (R/W)

3. **Register Name:** SPI_SLV_RD_BIT_REG
   **Address Offset:** 0x64

   - **Description:**
     - **Field Label:** (reserved)
     - **Field Bits:** [31, 24, 23] to [0]
     - **Reset Value:** 0x00000000
     - **Functionality:**
       - **SPI_SLV_RDATA_BIT**: It indicates the bit length of data the master reads from the slave, minus one.  
         *It is only valid in slave half-duplex mode.* (R/W)

4. **Register Name:** SPI_Wn_REG
   **Address Offset:** 0x80+4*n

   - **Description:**
     - **Field Label:** [31] to [0]
     - **Reset Value:** 0x00000000
     - **Functionality:**
       - **SPI_Wn REG**: Data buffer. (R/W)

**Footer Information:**
- Page Number: 378
- Document Version: ESP32 TRM (Version 5.6)
- Company Name and Submission Link:
  - Espressif Systems
  - Submit Documentation Feedback