**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Register Information:**
- **Register Name:** RTCIO_SENSOR_PADS_REG (0x007C)
- The register is a bit map with various sensor-related settings.

**Bit Map Description:**

1. **RTCCO_SENSOR_SENSEn_HOLD**: Set to 1 to hold the output value on sensen; 0 for normal operation.
   - Type: (R/W)

2. **RTCCO_SENSOR_SENSEn_MUX_SEL**: 
   - Route sensen to the RTC block or digital IO_MUX based on whether it is set to '1' or '0'.
   - Type: (R/W)
   
3. **RTCCO_SENSOR_SENSEn_FUN_SEL**:
   - Selects the RTC IO_MUX function for this pin.
     - 0 selects Function 0
   - Type: (R/W)

4. **RTCCO_SENSOR_SENSEn_SLP_SEL**:
   - Selection of sleep mode for the pin; set to '1' to put the pin in sleep mode during idle states or low power modes, otherwise it is disabled.
   - Type: (R/W)
   
5. **RTCCO_SENSOR_SENSEn_SLP_IE**:
   - Input enable of the pin in sleep mode
     - 1 enables; 0 disables 
   - Type: (R/W)

6. **RTCCO_SENSOR_SENSEn_FUN_IE**:
   - Input enable of the pin.
     - 1 enabled;
     - 0 disabled
   - Type: (R/W)

**Footer Information:**
- Page number: "155"
- Document version and source information at bottom right corner.

**Navigation Links:**
- GoBack

**Company Name:** Espressif Systems  
**Document Submission Feedback Link**: Submit Documentation Feedback