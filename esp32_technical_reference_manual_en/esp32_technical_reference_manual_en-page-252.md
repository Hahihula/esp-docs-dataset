**Chapter Title:**
Chapter 12 DPort Registers

**Section Header:**
Register 12.13. DPORT_APP_CACHE_CTRL1_REG (0x05C)

**Binary Diagram Description:**
A binary diagram is shown with various labels such as "DPRT APP CACHE_MMU_IA_CLR", "DPRT APP CACHE_MMU_PD", etc., indicating different bits in the register.

**Register Descriptions and Values:**

- **DPORT_APP_CACHE-MMU_IA_CLR**: Clears APP cache MMU error flag. (R/W)
  - Binary representation of values:
    ```
    31  | 14  | 13  | 12  | 11   | ... | 0
    ```

- **DPORT_APP_CACHE-MMU_PD**: Disables APP cache MMU.
  - (R/W)

- **DPORT_APP_CACHE_MASK_OPSDRAM**: Disables access from PRO_CPU DRAM to APP cache.
  - Values:
    ```
    1: Disable
    0: Enable
    ```

- **DPORT_APP_CACHE_MASK_DROMO**: Disables access from APP_CPU DROMO to APP cache.
  - Values:
    ```
    1: Disable
    0: Enable
    ```

- **DPORT_APP_CACHE_MASK_DRAM1**: Disables access from APP_CPU DRAM1 to APP cache.
  - Values:
    ```
    1: Disable
    0: Enable
    ```

- **DPORT_APP_CACHE_MASK_IROMO**: Disables access from APP_CPU IROMO to APP cache.
  - (R/W)

- **DPORT_APP_CACHE_MASK_IRAMI**: Disables access from APP_CPU IRAMI to APP cache.
  - Values:
    ```
    1: Disable
    0: Enable
    ```

- **DPORT_APP_CACHE_MASK_IRAMO**: Disables access from APP_CPU IRAMO to APP cache.
  - (R/W)

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32 TRM (Version 5.6)