**Title:**
Chapter 16 World Controller (WCL)

**GoBack**

**Section Title:**
Register 16.19. WCL_CORE_O_NMI_MASK_REG (0x0190)

**Body Text with Diagrams and Descriptions:**
- **Diagram Description:** Binary representation of the register.
  - **Text Below Diagram:** 
    ```
    31
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    (reserved)
    ```

- **Text Description:**
  - `WCL_CORE_O_NMI_MASK` Set this bit to mask all the NMI interrupts in CPUO. (R/W)

**Section Title:**
Register 16.20. WCL_CORE_O_NMI_MASK_PHASE_REG (0x0194)

**Body Text with Diagrams and Descriptions:**
- **Diagram Description:** Binary representation of another register.
  - **Text Below Diagram:**
    ```
    31
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    (reserved)
    ```

- **Text Description:**
  - `WCL_CORE_O_NMI_MASK_PHASE` Indicates if the NMI interrupt is being masked in CPUO. 
    ```
    1: masked; 0: not masked. (RO)
    ```

**Footer Information:**
Espressif Systems
821 ESP32-S3 TRM (Version 1.7)

**Link Texts:**
- Submit Documentation Feedback