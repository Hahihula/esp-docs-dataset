**Title:**
Chapter 10 Timer Group (TIMG)

**Subtitles and Sections with Descriptions of Registers:**

- **Register 10.22. TIMGn_INT_ST_REG (0x00a0)**
  - Description:
    ```
    TIMGn_INT_WDT_INT_ST
    The masked interrupt status bit for the TIMGn_INT_WDT_INT interrupt.
    (RO)
    
    TIMGn_INT_T1_INT_ST
    The masked interrupt status bit for the TIMGn_INT_T1_INT interrupt. (RO)
    
    TIMGn_INT_TO_INT_ST
    The masked interrupt status bit for the TIMGn_INT_TO_INT interrupt. (RO)
    ```

- **Register 10.23. TIMGn_INT_CLR_REG (0x00a4)**
  - Description:
    ```
    TIMGn_INT_WDT_INT_CLR
    Set this bit to clear the TIMGn_INT_WDT_INT interrupt. (WO)
    
    TIMGn_INT_T1_INT_CLR
    Set this bit to clear the TIMGn_INT_T1_INT interrupt. (WO)
    
    TIMGn_INT_TO_INT_CLR
    Set this bit to clear the TIMGn_INT_TO_INT interrupt. (WO)
    ```

**Footer:**
- "Espressif Systems"
- Page number and document version:
  ```
  ESP32 TRM (Version 5.6)
  ```