**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Section Heading:**
18.6 Registers

**Body Text:**
The addresses in this section are relative to the SHA accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subsection with Register Information:**

- **Register Name:** Register 18.1. SHA_START_REG (0x0010)
  - Description: Write 1 to start Typical SHA calculation.
  - Access Type: WO
  - Binary Representation Diagram:
    ```
    [31] | [30] | ... | [0]
    -------------------
    SHA_START
    ```

- **Register Name:** Register 18.2. SHA_CONTINUE_REG (0x0014)
  - Description: Write 1 to continue Typical SHA calculation.
  - Access Type: WO
  - Binary Representation Diagram:
    ```
    [31] | [30] | ... | [0]
    -------------------
    SHA_CONTINUE
    ```

- **Register Name:** Register 18.3. SHA BUSY_REG (0x0018)
  - Description: Indicates the states of SHA accelerator.
  - Access Type: RO
  - Binary Representation Diagram:
    ```
    [31] | [30] | ... | [0]
    -------------------
    SHA_BUSY_STATE
    ```

- **Register Name:** Register 18.4. SHA_DMA_START_REG (0x001C)
  - Description: Write 1 to start DMA-SHA calculation.
  - Access Type: WO
  - Binary Representation Diagram:
    ```
    [31] | [30] | ... | [0]
    -------------------
    SHA_DMA_START
    ```

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)