

```markdown
## 7.2.2 Architectural Overview

Figure 7.2-1. System Clock


## 7.2.3 Features

ESP32-C61 clocks can be classified into two types depending on their frequencies:

*   High-performance (HP) clocks for devices working at a higher frequency, such as CPU and digital peripherals
    *   PLL_F480M_CLK (480 MHz): internal PLL clock. Its reference clock is XTAL_CLK
    *   XTAL_CLK (40 MHz): external crystal clock

*   Low-power (LP) clocks for low-power system and some peripherals working in low-power mode
    *   XTAL32K_CLK (32 kHz): external crystal clock
    *   RC_FAST_CLK (20 MHz by default): internal fast RC oscillator with adjustable frequency
    *   RC_SLOW_CLK (130 kHz by default): internal slow RC oscillator with adjustable frequency
    *   OSC_SLOW_CLK (32 kHz by default): external slow clock input through XTAL_32K_P. After configuring this GPIO, also configure the Hold function (see Chapter 6 GPIO Matrix and IO MUX >
```