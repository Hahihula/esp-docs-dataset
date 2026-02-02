**Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Diagram Labels and Descriptions for Figure 9.3-6, RTC Low-Power Clocks**

- **Selection Signal:** 
  - RC_SLOW_CLK connected to RTC_Tmer.
  - XTAL32K_CLK not used in this configuration.

- **Selection Signal:**
  - RTC_FAST_DIV_1 CLK is selected and goes through the path:
    - RTC_Main State
    - PMU

**Diagram Labels for Figure 9.3-7, Digital Low-Power Clocks**

- Selection Signals include RC_SLOW_CLK, RTC_SLOW_CLK, RC_FAST_CLK.
- The signal paths are as follows:

1. **RC_SLOW_CLK**
   - Goes to the selection point.

2. **RTC_SLOW_CLK**
   - Goes through LP_MUX and then splits into two directions:
     - One path goes towards Wireless (labeled LOW_POWER_CLK).
     - Another branch is not specified in detail but it seems connected further down, possibly indicating another component or connection within the system.
   
3. **RC_FAST_CLK**
   - Also passes through a selection point.

**Text:**

"For the digital core, LOW_POWER_CLK is switched among four sources. For details, please see Figure 9.3-7."

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)