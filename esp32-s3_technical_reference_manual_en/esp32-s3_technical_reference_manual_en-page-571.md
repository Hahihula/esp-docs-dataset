**Title: Chapter 10 Low-power Management (RTC_CNTL)**

---

### Figure Description:
- **Figure Title:** Wireless Clocks  
- **Diagram Components and Connections:**
  - XTAL32K_CLK connected to LP_MUX.
  - RC_FAST_CLK divided by n, labeled as div n in the diagram box within LP_MUX block.
  - RTC_SLOW_CLK also connects into LP_MUX but is not further subdivided or specified on this page.

### Table:
- **Table Title:** Low-Power Clocks  
- **Table Columns:**
  - "Clock Type"
  - "Clock Source"
  - "Selection Option"
  - "Effective for"

| Clock Type       | Clock Source                   | Selection Option                                      | Effective for                                    |
|------------------|--------------------------------|-------------------------------------------------------|--------------------------------------------------|
| RTC Slow Clock   | XTAL32K_CLK                    | RTC_CNTL_ANA_CLK_RTC_SEL                              | Power management unit                             |
|                  | RC_FAST_DIV_CLK                |                                                      | RTC Timers                                       |
|                  | RC_SLOW_CLK (Default)         |                                                      | ULP Timers                                       |
|                  | RC_FAST_CLK divided by n      |                                                      | ULP co-processor                                 |
| **(Default)**    |                                |                                                      | Sensor controller                                |
| RTC Fast Clock   |                                | RTC_CNTL_FAST_CLK_RTC_SEL                            | RTC registers                                    |
|                  | XTAL_DIV_CLK                   |                                                      | RTC slow memory                                   |
|                  | XTAL32K_CLK                    | SYSTEM_LPCLK_SEL_XTAL32K                              | Wireless modules (Wi-Fi/BT)                      |
| **Wireless Clock**| RC_FAST_CLK divided by n      | SYSTEM_LPCLK_SEL_8M                                  | in the digital domain working                     |
|                  | RTC SLOW CLK                   | SYSTEM_LPCLK_SEL_RTC_SLOW                           | in low-power modes                               |

---

### Text:
- For more detailed description about clocks, please refer to 7 Reset and Clock.

**Subtitle:**
10.3.3 Timers

ESP32-S3’s low-power management uses 3 timers:

- RTC timer
- ULP timer
- Touch timer

This section only introduces the RTC timer. For detailed description of ULP timer, please refer to Chapters 2 and later.

---

**Footer:**
Espressif Systems  
571 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback