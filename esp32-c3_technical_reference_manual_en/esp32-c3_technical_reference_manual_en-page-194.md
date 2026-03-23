

```markdown
## 6.2.2 Architectural Overview

Figure 6.2-1. System Clock


### 6.2.3 Features

ESP32-C3 clocks can be classified in two types depending on their frequencies:

*   High speed clocks for devices working at a higher frequency, such as CPU and digital peripherals
    *   PLL_CLK (320 MHz or 480 MHz): internal PLL clock
    *   XTAL_CLK (40 MHz): external crystal clock

*   Slow speed clocks for low-power devices, such as RTC module and low-power peripherals
    *   XTAL32K_CLK (32 kHz): external crystal clock
    *   RC_FAST_CLK (17.5 MHz by default): internal fast RC oscillator with adjustable frequency
    *   RC_FAST_DIV_CLK: internal fast RC oscillator derived from RC_FAST_CLK divided by 256
    *   RC_SLOW_CLK (136 kHz by default): internal low RC oscillator with adjustable frequency


### 6.2.4 Functional Description
```