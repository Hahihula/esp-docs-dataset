Title: Chapter 12 Timer Group (TIMG)

Subheading: GoBack

### 12.2.4 Timer Reload

A timer is reloaded when a timer’s current value is overwritten with a reload value stored in the TIMG_Tx_LOAD_LO and TIMG_Tx_LOAD_HI fields that correspond to the lower 32-bits and higher 22-bits of the timer's new value, respectively. However, writing a reload value to TIMG_Tx_LOAD_LO and TIMG_Tx LOAD_HI will not cause the timer’s current value to change. Instead, the reload value is ignored by the timer until a reload event occurs. A reload event can be triggered either by a software instant reload or an auto-reload at alarm.

A software instant reload is triggered by the CPU writing any value to TIMG_Tx LOAD_REG, which causes the timer’s current value to be instantly reloaded. If TIMG_Tx_EN is set, the timer will continue incrementing or decrementing from the new value. If TIMG_Tx_EN is cleared, the timer will remain frozen at the new value until counting is re-enabled.

An auto-reload at alarm will cause a timer reload when an alarm occurs, thus allowing the timer to continue incrementing or decrementing from the reload value. This is generally useful for resetting the timer’s value when using periodic alarms. To enable auto-reload at alarm, the TIMG_Tx_AUTORELOAD field should be set. If not enabled, the timer's value will continue to increment or decrement past the alarm value after an alarm.

### 12.2.5 RTC_SLOW_CLK Frequency Calculation

Via XTAL_CLK, a timer could calculate the frequency of clock sources for RTC_SLOW_CLK (i.e., RC_SLOW_CLK, RC_FAST_DIV_CLK, and XTAL32K_CLK) as follows:

- Start periodic or one-shot frequency calculation;
- Once receiving the signal to start calculation, the counter of XTAL_CLK and the counter of RTC_SLOW_CLK begin to work at the same time. When the counter of RTC_SLOW_CLK counts to CO, the two counters stop counting simultaneously;
- Assume the value of XTAL_CLK’s counter is C1, and the frequency of RTC_SLOW_CLK would be calculated as: \( f_{r_t c} = \frac{C_0 \times f_{X T A L\_C L K}}{C_1} \)

### 12.2.6 Interrupts

Each timer has its own interrupt line that can be routed to the CPU, and thus each timer group has a total of three interrupt lines. Timers generate level interrupts that must be explicitly cleared by the CPU on each triggering.

Interrupts are triggered after an alarm (or stage timeout for watchdog timers) occurs. Level interrupts will be held high after an alarm or until it is manually cleared to enable a timer’s interrupt, the TIMG_Tx_INT_ENA bit should be set.
The interrupts of each timer group are governed by a set of registers. Each timer within the group has a corresponding bit in these registers:

- TIMG_Tx_INT_RAW: An alarm event sets it to 1. The bit will remain set until the timer’s corresponding bit in TIMG_Tx_INT_CLR is written.
- TIMG_WDT_INT_RAW: A stage timeout will set the timer's bit to 1. It remains set for a while, and then cleared when the timer’s corresponding bit in TIMG_WDT_INT_CLR is written.

Footer:
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback