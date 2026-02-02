**Chapter Title:**
Chapter 12 DPort Registers

**Section Header:**
Register 12.200, DPORT_CACHE_ACCESS_ILLEGAL_INT_EN_REG (0x3A0)

**Table Description:**
- The table shows the bit positions and their corresponding descriptions for various registers related to cache access interrupts.
- Bits are labeled from rightmost side as follows:
  - Bit 31
  - Bit 28, etc. down to bits 6

**Bit Descriptions in Markdown Format with Code Blocks:**

### DPORT_PRO_CACHE_ACCESS_ILLEGAL_INT_EN
Enables the PRO CPU’s illegal access to CACHE address region interrupt.

- **Bit Description:** 
  - Bit 0:
    ```plaintext
    Enables the APP CPU's illegal access to VAddrRAM (low-high mode) address region interrupt.
    ```
  - Bit 1: 
    ```plaintext
    Enables the PRO CPU's illegal access to VAddrRAM address region interrupt
    ```
  - Bit 2: 
    ```plaintext
    Enables the PRO CPU's illegal access to VAddr3 address region interrupt
    ```
  - Bit 3:
    ```plaintext
    Enables the PRO CPU's illegal access to VAddr2 address region interrupt
    ```
  - Bit 4:
    ```plaintext
    Enables the PRO CPU's illegal access to VAddr1 address region interrupt
    ```
  - Bit 5: 
    ```plaintext
    Enables the PRO CPU's illegal access to VAddr4 address region interrupt (RO)
    ```

### DPORT_PRO_CACHE_MMU_ILLEGAL_INT_EN
Enables the PRO CPU’s access to invalid CACHE entry. (RO)

### DPORT_APP_CACHE_ACCESS_ILLEGAL_INT_EN
Enables the APP CPU’s illegal access to CACHE address region interrupt.

- **Bit Description:** 
  - Bit 0:
    ```plaintext
    Enables the PRO CPU's illegal access to RVAddrRAM (low-high mode) address region interrupt
    ```
  - Bit 1: 
    ```plaintext
    Enables the APP CPU's illegal access to VAddrRAM address region interrupt
    ```
  - Bit 2: 
    ```plaintext
    Enables the APP CPU’s illegal access to VAddr3 address region interrupt
    ```
  - Bit 3:
    ```plaintext
    Enables the APP CPU’s illegal access to VAddr2 address region interrupt
    ```
  - Bit 4:
    ```plaintext
    Enables the APP CPU's illegal access to VAddr1 address region interrupt
    ```
  - Bit 5: 
    ```plaintext
    Enables the APP CPU’s illegal access to VAddr4 address region interrupt (RO)
    ```

### DPORT_APP_CACHE_MMU_ILLEGAL_INT_EN
Enables the APP CPU’s access to invalid CACHE entry. (RO)

**Footer Information:**  
Espressif Systems  
269 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback