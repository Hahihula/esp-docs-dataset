**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Navigation Link:**
GoBack

**Section Header and Description:**
Register 30.8. SPI_MISC_REG (For SPI2 Only) (0x0020)

**Continuation Note:**
Continued from the previous page...

**List of Registers with Descriptions:**

- **SPI_DQS_IDLE_EDGE**: The default value of SPI_DQS. 0: low voltage level; 1: high voltage level. Can be configured in CONF state. (R/W)
  
- **SPI_CK_IDLE EDGE**: 
  - Description for register:
    - GP-SPI2 is idle.
    - Can be configured in CONF state.

- **SPI_CS_KEEP_ACTIVE**:
  - Description of the line behavior when bit set: SPI CS line keeps low
  - Can be configured in CONF state. (R/W)

- **SPI_QUAD_DIN_PIN_SWAP**:
  - Description for swap functionality with FSPIH/0.
    - Swap FSPID with FSPIQ, swap FSPIWP

**Footer Information:**
Espressif Systems  
1160  
ESP32-S3 TRM (Version 1.7)  

**Link at the bottom of page:** 
Submit Documentation Feedback