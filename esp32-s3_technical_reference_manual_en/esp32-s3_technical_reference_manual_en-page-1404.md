**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Menu:**
GoBack

**Section Title:**
Register 36.66. MCPWM_CAP_CH2_REG (0x104)

**Field Description and Values:**
- **MCPWM_CAP2_VALUE**: Value of last capture on channel 2.
  - (RO)
  
**Section Title:**
Register 36.67. MCPWM_CAP_STATUS_REG (0x108)

**Field Description with Bits Indication:**
- **(reserved)**
- **MCPWM_CAP0_EDGE**: Edge of last capture trigger on channel 0, 0: rising edge, 1: falling edge.
  - (RO)
- **MCPWM_CAP1_EDGE**: Edge of last capture trigger on channel 1, 0: rising edge, 1: falling edge. 
  - (RO)
- **MCPWM_CAP2_EDGE**: Edge of last capture trigger on channel 2, 0: rising edge, 1: falling edge.
  - (RO)

**Footer Information:**
Espressif Systems
Page number and document version:
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback