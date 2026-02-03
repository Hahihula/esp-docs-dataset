**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**Section Titles and Content:**

- **5. Handle the alarm interrupt.**
  - Clear the interrupt by setting the timer’s corresponding bit in TIMG_Tx_INT_CLR.
  - Disable the timer by clearing TIMG_Tx_EN.

- **12.3.3 Timer as Periodic Alarm**
  1. Configure the time-base counter following step 1 in Section 12.3.1.
  2. Configure the alarm following step 2 in Section 12.3.2.
  3. Enable auto reload by setting TIMG_Tx_AUTORELOAD and configure the reload value via TIMG_Tx_LOAD_LO and TIMG_Tx_LOAD_HI.
  4. Start the alarm by setting TIMG_Tx_ALARM_EN.
  5. Handle the alarm interrupt (repeat on each alarm iteration).
     - Clear the interrupt by setting the timer’s corresponding bit in TIMG_Tx_INT_CLR.
     - If the next alarm requires a new alarm value and reload value, i.e., different alarm interval per iteration), then TIMG_TxALARMLO_REG, TIMG_TxALARMHI_REG, TIMG_Tx_LOAD_LO, and TIMG_Tx_LOAD_HI should be reconfigured as needed. Otherwise, the aforementioned registers should remain unchanged.
  - Re-enable the alarm by setting TIMG_Tx_ALARM_EN.

- **6. Stop the timer (on final alarm iteration).**
  Clear the interrupt by setting the timer’s corresponding bit in TIMG_Tx_INT_CLR.
  Disable the timer by clearing TIMG_Tx_EN.

- **12.3.4 RTC_SLOW_CLK Frequency Calculation**

  - **One-shot frequency calculation:**
    1. Select the clock whose frequency is to be calculated (clock source of RTC_SLOW_CLK) via TIMG_RTC_CALI_CLK_SEL, and configure the time of calculation via TIMG_RTC_CALI_MAX.
       - Select one-shot frequency calculation by clearing TIMG_RTC_CALI_START_CYCLING, and enable the two counters via TIMG_RTC_CALI_START.
    2. Once TIMG_RTC_CALI_RDY becomes 1, read TIMG_RTC_CALI_VALUE to get the value of XTAL_CLK’s counter, and calculate the frequency of RTC_SLOW_CLK.

  - **Periodic frequency calculation:**
    Select the clock whose frequency is to be calculated (clock source of RTC_SLOW_CLK) via TIMG_RTC_CALI_CLK_SEL, and configure the time of calculation via TIMG_RTC_CALI_MAX.
    - Select periodic frequency calculation by enabling TIMG_RTC_CALI_START_CYCLING.

  - **When TIMG_RTC_CALI_CYCLING_DATA_VLD is 1, TIMG_RTC_CALI_VALUE is valid.**

- **Timeout**
  If the counter of RTC_SLOW_CLK cannot finish counting in TIMG_RTC_CALI_TIMEOUT_RST_CNT cycles,
  TIMG_RTC_CALI_TIMEOUT will be set to indicate a timeout.

**Footer:**
Espressif Systems
659 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback