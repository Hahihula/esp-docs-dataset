

```markdown
Figure 9.3-4. Wireless Clock


Table 9.3-1. Low-power Clocks

| Clock Type         | Clock Source                                                                 | Selection Signal                                      | Power Domain                     |
|--------------------|------------------------------------------------------------------------------|------------------------------------------------------|----------------------------------|
| RTC Fast Clock     | RC_FAST_CLK divided by n (Default)<br>XTAL_DIV_CLK<br>XTAL32K_CLK          | RTC_CNTL_FAST_CLK_RTC_SEL                            | RTC Registers                   |
| RTC Slow Clock     | RC_FAST_DIV_CLK<br>RC_SLOW_CLK (default)                                    | RTC_CNTL_ANA_CLK_RTC_SEL                             | Power Management System (except RTC registers) |
| Wireless Clock     | XTAL32K_CLK<br>RC_FAST_CLK divided by n<br>RTC_SLOW_CLK<br>XTAL_CLK         | SYSTEM_LPCLK_SEL_XTAL32K<br>SYSTEM_LPCLK_SEL_20M<br>SYSTEM_LPCLK_RTC_SLOW<br>SYSTEM_LPCLK_SEL_XTAL | Wireless modules (Wi-Fi/BT) in the digital system domain working in low-power modes |

When working under low-power modes, ESP32-C3's XTAL_CLK and PLL are usually powered down to reduce power consumption. However, the low-power clock remains on so the chip can operate properly under low-power modes. For more detailed description about clocks, please refer to 6 Reset and Clock.

9.3.3 Timers

ESP32-C3's low-power management uses RTC timer. The readable 48-bit RTC timer is a real-time counter (using RTC slow clock) that can be configured to log the time when one of the following events happens. For details, see Table 9.3-2.

Table 9.3-2. The Triggering Conditions for the RTC Timer

| Enabling Options | Descriptions |
```