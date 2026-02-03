**Chapter Title:**
Chapter 14 XTAL32K Watchdog Timers (XTWDT)

**Section Titles and Content:**

- **14.2.2 BACKUP32K_CLK**
  - Once the XTAL32K watchdog timer detects the oscillation failure of XTAL32K_CLK, it replaces XTAL32K_CLK with BACKUP32K_CLK (with a frequency of 32 kHz or so) derived from RC_SLOW_CLK as RTC_SLOW_CLK to ensure proper functioning of the system.

- **14.3 Functional Description**

  - **14.3.1 Workflow**
    1. The XTAL32K watchdog timer starts counting when RTC_CNTL_XTAL32K_WDT_EN is enabled. The counter based on RC_SLOW_CLK keeps counting until it detects the positive edge of XTAL_32K and is then cleared. When the counter reaches RTC_CNTL_XTAL32K_WDT_TIMEOUT, it generates an interrupt or a wake-up signal and is then reset.
    2. If RTC_CNTL_XTAL32K_AUTO_BACKUP is set and step 1 is finished, the XTAL32K watchdog timer will automatically enable BACKUP32K_CLK as the alternative clock source of RTC_SLOW_CLK, to ensure the system’s proper functioning and the accuracy of timers running on RTC_SLOW_CLK (e.g., RTC_TIMER). For information about clock frequency configuration, please refer to Section 14.3.2.
    3. To restore the XTAL32K watchdog timer, software restarts XTAL32K_CLK by turning its XPD (meaning no power-down) signal off and on again via RTC_CNTL_XPD_XTAL_32K bit. Then, the XTAL32K watchdog timer switches back to XTAL32K_CLK as the clock source of RTC_SLOW_CLK by clearing RTC_CNTL_XTAL32K_WDT_EN (BACKUP32K_CLK_EN is also automatically cleared). If the chip is in Light-sleep or Deep-sleep mode, the XTAL32K watchdog timer will wake up the CPU to finish the above steps.

- **14.3.2 BACKUP32K_CLK Working Principle**
  - Chips have different RC_SLOW_CLK frequencies due to production process variations. To ensure the accuracy of RTC_TIMER and other timers running on RTC_SLOW_CLK when BACKUP32K_CLK is at work, the divisor of BACKUP32K_CLK should be configured according to the actual frequency of RC_SLOW_CLK (see details in Chapter 10 Low-power Management (RTC_CNTL)) via RTC_CNTL_XTAL32K_CLK_FACTOR_REG register. Each byte in this register corresponds to a divisor component (\(x_0 \sim x_{6}\)). BACKUP32K_CLK is divided by a fraction where the denominator is always 4, as calculated below.
    - \(f_{back_clk}/4 = f_{rc_slow_clk}/S\)
    - Where:
      - \(S = x_0 + x_1 + \ldots + x_7\)

- **14.3.3 Configuring the Divisor Component of BACKUP32K_CLK**
  - Based on principles described in Section 14.3.2, you can configure the divisor component as follows:
    - \(f_{back_clk} = \text{desired frequency of BACKUP32K_CLK; } f_{rc_slow_clk} = \text{actual frequency of RC_SLOW_CLK}\)
    - \(x_0 \sim x_7\) correspond to the pulse width in high and low state for four BACKUP32K_CLK clock signals (unit: RC_SLOW_CLK clock cycle).

**Footer Information:**
- Page number 681
- Document version ESP32-S3 TRM (Version 1.7)
- Company name Espressif Systems

**Navigation Links:** 
- GoBack button at the top right corner of each section.

**Action Button:**
- Submit Documentation Feedback link available on page footer for user interaction.