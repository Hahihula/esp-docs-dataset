**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Register Information (Section Header):**
Register 39.2. RTC_CNTL_TOUCH_CTRL2_REG (0x10C)

**Table Description with Labels, Bits, and Values for Each Bit Field:**
- RTC_CNTL_TOUCH_CLKGATE_EN
- RTC_CNTL TOUCH_CLK FO
- RTC_CNTL_TOUCH_RESET
- RTC_CNTL_TOUCH_TIMER_FORSLP_DIV
- RTC_CNTL_TOUCH_XPD_WAIT
- RTC_CNTL_TOUCH_STARTForce
- RTC_CNTL_TOUCH_FSM_EN
- RTC_CNTL_TOUCH_DRIASRefC
- RTC_CNTL_TOUCH_XPD_BIAS
- RTC_CNTL_TOUCH_DREFH
- RTC_CNTL TOUCH_DREFL
- RTC_CNTL TOUCH_DRANGE

**Bit Fields Description:**
- 31 to 24 bits are labeled with the corresponding register names.
- Bits from position (0x4) down.

**Field Descriptions and Values in Hexadecimal Format for Each Bit Field:**
- RTC_CNTL_TOUCH_DRANGE:
  - Touch attenuation. (R/W)
  - Value range is shown as "0x4".
  
- RTC_CNTL TOUCH_DREFL:
  - Touch reference voltage low.
  - Range of values provided are from `0` to `3`.

- RTC_CNTL TOUCH_DREFH:
  - Touch reference voltage high.

**Field Descriptions for Other Registers:**
- RTC_CNTL_TOUCH_XPD_BIAS (R/W):
  - Touch bias power switch. 

- RTC_CNTL TOUCH_REFC:
  - Touch pin O reference capacitance.
  
- RTC_CNTL TOUCH_DBIAS:
  - Use self bias or use bandgap bias, with options `1` and `0`.

- RTC_CNTL TOUCH_SLP_TIMER_EN (R/W):
  - Timer enable bit.

- RTC_CNTL TOUCH_START_FSM_EN: 
  - TOUCH_START and TOUCH_XPD are controlled by touch FSM.
  
- RTC_CNTL TOUCH_START_EN:
  - Start touch FSM, valid when RTC_CNTL TOUCH_START FORCE = `1`.

- RTC_CNTL TOUCH_STARTFORCE (R/W):
  - Start touch FSM by software or timer.

- RTC_CNTL TOUCH_XPD_WAIT: 
  - The waiting cycles between TOUCH_START and TOUCH_XPD.
  
**Footer Information:** Continued on the next page...

**Company Logo/Name at Bottom Left Corner:**
Espressif Systems

**Document Footer (Bottom Right):**
1481 ESP32-S3 TRM (Version 1.7)

**Feedback Link:** Submit Documentation Feedback