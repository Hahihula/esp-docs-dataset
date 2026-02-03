**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Register Information:**
- Register Name: I2S_RX_TDM_CTRL_REG (0x0050)
- Bit Description:
  - Bits [31] to [0]: Reserved

**Bit Definitions and Functions:**

- **I2S_RX_TDM_PDM_CHAN1_EN:** 
  - Function: Enable the valid data input of I2S RX TDM or PDM channel. Channel selection is specified by bits.
  - Values:
    - `0`: Disable
    - `1`: Enable

**Detailed Descriptions for Each Channel:**

- **I2S_RX_TDM_PDM_CHAN1_EN:** 
  - Description: Enable the valid data input of I2S RX TDM or PDM channel. Channel selection is specified by bits.
  - Values:
    - `0`: Disable
    - `1`: Enable

- **I2S_RX_TDM_PDM_CHAN2_EN**
  - Description: Enable the valid data input of I2S RX TDM or PDM channel for specific channels (2,3,...).
  - Values and Channels:
    - Channel selection is specified by bits.
    - `0`: Disable
    - `1`: Enable

- **Continuation Note:** Continued on the next page...

**Footer Information:**
- Company Name: Espressif Systems
- Document Version: ESP32-S3 TRM (Version 1.7)
- Page Number and Link:
  - "Submit Documentation Feedback" link at bottom of document.

This structured description captures all textual content from the image, including register information, bit definitions with their functions for each I2S channel control in a detailed manner as per your request without adding any conversational text or interpreting diagrams.