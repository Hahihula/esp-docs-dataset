**Chapter Title:**
Chapter 23 External Memory Encryption and Decryption (XTS_AES)

**Section Heading:**
23.7 Registers

**Body Text:**
The addresses in this section are relative to the External Memory Encryption and Decryption base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subsection Title:**
Register 23.1. XTS_AESPLAIN_n_REG (n: O-15) (0x0000+4*n)

**Table Description for Register 23.1:**
- **Column Headers:** 
  - Address
  - Data

- **Row Content:**
  - Address: `0x000000`
  - Data: `[Empty]` (with a reset indicator)
  
- **Description of the Register:**
  XTS_AESPLAIN_n Registers nth 32-bit piece of plain text. (R/W)

**Subsection Title:**
Register 23.2. XTS_ALINESIZE_REG (0x0040)

**Table Description for Register 23.2:**
- **Column Headers:** 
  - Address
  - Data

- **Row Content:**
  - Address: `[Empty]`
  - Data: `[Empty]` (with a reset indicator)
  
- **Description of the Register:**
  XTS_ALINESIZE Configures the data size of one encryption.
    - `0`: 16 bytes;
    - `1`: 32 bytes;
    - `2`: 64 bytes. (R/W)

**Subsection Title:**
Register 23.3. XTS_AESTDESTINATION_REG (0x0044)

**Table Description for Register 23.3:**
- **Column Headers:** 
  - Address
  - Data

- **Row Content:**
  - Address: `[Empty]`
  - Data: `[Empty]` (with a reset indicator)
  
- **Description of the Register:**
  XTS_AESTDESTINATION Configures the type of external memory. Currently, it must be set to `0`, as the Manual Encryption block only supports flash encryption. Errors may occur if users write
    - `1`: O: flash; 1: external RAM.

**Footer Information:**
Espressif Systems  
916  
ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
- Submit Documentation Feedback

(Note: The actual content of the addresses and data fields in each table are not provided, only placeholders or empty cells with reset indicators.)