**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Section Header:**
Register 37. RMT_CHnCONFO_REG (n: 0-3) (0x0020+0x4*n)

**Continuation Note:**
Continued from the previous page...

**Body Text with Descriptions and Codes:**

1. **RMT_CARRIER_EFF_EN_CHn**
   - Description:
     Add carrier modulation on the output signal only at data-sending state for channel n.
   - Code (n): 0
   - Additional Info:
     Add carrier modulation on the output signal at data-sending state and idle state for channel. Only valid when RMT_CARRIER_EN_CHn is 1.

2. **RMT_CARRIER_EN_CHn**
   - Description:
     This is the carrier modulation enable-bit for channel n.
   - Code (n): 0
   - Additional Info:
     Add carrier modulation on the output signal: No Carrier modulation added on output signal

3. **RMT_CARRIER_OUT_LV_CHn**
   - Description:
     This bit is used to configure the position of carrier wave for channel n.

4. **RMT_CONF_UPDATE_CHn**
   - Description:
     Synchronization bit for channel (WT)

5. **RMT_DMA_ACCESS_EN_CH3**
   - Description:
     Reserved for channel 0-2
   - Additional Info:
     DMA access enable bit for channel

**Footer:**
Espressif Systems  
1428 ESP32-S3 TRM (Version 1.7)  

**Link Texts at the Bottom of Page:**
Submit Documentation Feedback