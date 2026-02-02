**Chapter Title:**
Chapter 10 Timer Group (TIMG)

**GoBack Link:** GoBack

---

**Register Information and Descriptions:**

- **Register 10.16, TIMGn_WDTFEED_REG (0x0060)**
  - **Field Description**: 
    ```
    TIMGn_WDTFEED_REG
    ```
  - **Hexadecimal Value Example**: `0x00000000`
  - **Reset Value**: Reset

- **Register 10.17, TIMGn_WDTWPROTECT_REG (0x0064)**
  - **Field Description**:
    ```
    TIMGn_WDTWPROTECT_REG
    ```
  - **Hexadecimal Value Example**: `0x050D83AA`
  - **Reset Value**: Reset

- **Register 10.18, TIMGn_RTCCALIFCFG_REG (0x0068)**
  - **Fields Description**:
    ```
    TIMGn_RTC_CALI_START_MAX
    TIMGn_RTC_CALI_START
    TIMGn_RTC_CALI_START_CYCLING
    TIMGn_RTC_CALI_START
    TIMGn_RTC_CALI_START
    TIMGn_RTC_CALI_START
    TIMGn_RTC_CALI_START
    ```
  - **Hexadecimal Value Example**: `0x01`
  - **Reset Value**: Reset

- **Field Description**:
  ```
  TIMGn_RTC_CALI_START_CYCLING Reserved. (R/W)
  ```

- **Field Description**:
  ```
  TIMGn_RTC_CALI_CLK_SEL Used to select the clock to be calibrated.
    0: RC_SLOW_CLK
    1: RC_FAST_DIV_CLK, 2: XTAL32K_CLK. (R/W)
  ```

- **Field Description**:
  ```
  TIMGn_RTC_CALI_RDY Set this bit to mark the completion of calibration. (RO)
  ```

- **Field Description**:
  ```
  TIMGn_RTC_CALI_MAX Calibration time, in cycles of the clock to be calibrated.
    (R/W)
  ```

- **Field Description**:
  ```
  TIMGn_RTC_CALI_START Set this bit starts calibration. (R/W)
  ```

---

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)