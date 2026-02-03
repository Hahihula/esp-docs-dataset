**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

**Register Information Section:**

- **Register Name and Address:**
  - Register 34.36, SDHOST_BUFAADDR_REG (0x0098)
  
- **Description of Register 34.36:**
  - "SDHOST_BUFAADDR_REG Host Buffer Address Pointer, updated by IDMAC during operation and cleared on reset. This register points to the current Data Buffer Address being accessed by the IDMAC. (RO)"
  
- **Register Name and Address:**
  - Register 34.37, SDHOST_CARDTHRCTL_REG (0x100)
  
**Diagram Description for Registers:**

- Diagram showing relationships between various registers:
  - "SDHOST_CARDTHRCTL_REG" is connected to other registers like "SDHOST_BUFAADDR_REG", and there are indications of reset states.
  - The diagram includes labels such as "SDHOST CARD THRCRTHREN REG", "SDHOST CARD WRTHREN REG", etc.

**Register Details:**

- **SDHOST_CARDTHRESHOLD_REG (0x100):**
  - Description:
    - "The inside FIFO size is 512. This register is applicable when SDHOST_CARDERTHREN_REG is set to 1 or SDHOST_CARDRDTHREN_REG set to 1."
  
- **SDHOST_CARDWRTHREN:**
  - Applicable condition and description for HS400 mode:
    - "Applicable when HS400 mode is enabled. (R/W)"
    - Example values with descriptions in hexadecimal format.
  
- **SDHOST_CARDCLRIENTEN:**
  - Description of interrupt generation status:
    - "Busy clear interrupt generation: (R/W)"
    - Example states and their meanings.

- **SDHOST_CARDRDTHREN:**
  - Card read threshold enable description for R/W mode with example values.
  
**Footer Information:**

- Company Name: Espressif Systems
- Document Version: ESP32-S3 TRM (Version 1.7)
- Link to Submit Documentation Feedback

(Note: The text in the diagram is not fully transcribed due to complexity and potential need for visual inspection.)