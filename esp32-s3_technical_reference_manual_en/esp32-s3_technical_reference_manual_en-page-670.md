**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**Section Titles and Descriptions with Registers Information:**

- **Register 12.23. TIMG_INT_ST_TIMERS_REG (0x0078)**
  - Description:
    ```
    TIMG_TX_INT_ST
      The masked interrupt status bit for the TIMG_Tx_INT interrupt.
      (RO)
    
    TIMG_WDT_INT_ST
      The masked interrupt status bit for the TIMG_WDT_INT interrupt. 
      (RO)
    ```

- **Register 12.24. TIMG_INT_CLR_TIMERS_REG (0x007C)**
  - Description:
    ```
    TIMG_TX_INT_CLR
      Set this bit to clear the TIMG_Tx_INT interrupt.
      (WT)
    
    TIMG_WDT_INT_CLR
      Set this bit to clear the TIMG_WDT_INT interrupt. 
      (WT)
    ```

- **Register 12.25. TIMG_NTIMERS_DATE_REG (0x0F8)**
  - Description:
    ```
    TIMG_NTIMERS_DATE
      Timer version control register.
      (R/W)
    ```

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number and Document Version Information:**  
ESP32-S3 TRM (Version 1.7)