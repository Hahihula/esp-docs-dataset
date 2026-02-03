**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.22. RTC_CNTL_RTC_EXT_XTL_CONF_REG (0x0060)

**Body Text and Descriptions for Registers:**

- **Continued from the previous page...**
  
  - **RTC_CNTL_DRES_XTAL_32K**: DRES_XTAL_32K (R/W)
    - Description not provided.
    
  - **RTC_CNTL_XPD_XTAL_32K**: XPD_XTAL_32K (R/W)
    - Description not provided.
    
  - **RTC_CNTL_DAC_XTAL_32K**: DAC_XTAL_32K (R/W)
    - Description not provided.
    
  - **RTC_CNTL_RTC_WDT_STAT**: Stores the status of the 32 kHz watchdog. (RO)
    - Description not provided.
    
  - **RTC_CNTL_RTC_XTAL32K_GPIO_SEL**: Selects the 32 kHz crystal clock. 0: selects the external 32 kHz clock; 1: selects clock from the RTC GPIO X32P_C. (R/W)
    - Description not provided.
    
  - **RTC_CNTL_XTL_EXT_CTR_LV**: 0: powers down XTAL at high level, 1: powers down XTAL at low level
    - Description of register function is "Enables the GPIO to power down the crystal oscillator." (R/W)
    
- **Register Title and Description for Register 10.23**:
  
  - **RTC_CNTL_RTC_EXT_WAKEUP_CONF_REG (0x0064)**
    - **RTC_CNTL_XTL_WAKEUP_LV**: 
      - Description not provided.
      
    - **RTC_CNTL_GPIO_WAKEUP_FILTER**:
      - Set this bit to enable the GPIO wakeup event filter. (R/W)
    
    - **RTC_CNTL_EXT_WAKEUP_LV**:
      - 0: external wakeup O at low level, 1: external wakeup O at high level
        - Description not provided.
      
    - **RTC_CNTL_EXT_WAKEUP1_LV**:
      - 0: external wakeup 1 at low level, 1: external wakeup 1 at high level

**Footer Information:**
Espressif Systems  
605 ESP32-S3 TRM (Version 1.7)  

**Navigation Links:**
- Submit Documentation Feedback
- GoBack