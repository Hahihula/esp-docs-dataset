**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Subtitle:**
10.3.2 Low-Power Clocks

**Body Text:**
In general, ESP32-S3 powers down its external crystal XTAL_CLK and PLL to reduce power consumption when working in low-power modes. During this time, the chip's low-power clocks remain on to provide clocks to different power domains, such as the power management unit, RTC peripherals, RTC fast memory, RTC slow memory, and wireless circuits in the digital domain.

**Diagram Description:**
- The diagram is labeled "Figure 10.3-3. RTC Clocks".
- It shows a block diagram with two selection signals (labeled '0' for RC_SLOW_CLK and XTAL_32K_CLK; labled '1' for RC_FAST_DIV_CLK).
- There are connections from the selection signal to different components:
  - For "RC_SLOW_CLK":
    - PMU
    - RTC_SLOW_CLK
  - For "XTAL_32K_CLK":
    - RTC_SLOW_CLK
  - For "RC_FASTDIV_CLK":
    - RTC_Timer
    - ULP Timer
- Another selection signal is shown for the component labeled as "ULP Coprocessor".
- There are additional connections:
  - XTAL_DIV_CLK to Sensor Controller and RTC_FAST_CLK.
  - RC_FAST_CLK to div n, which then connects back to RTC_SLOW_CLK.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)