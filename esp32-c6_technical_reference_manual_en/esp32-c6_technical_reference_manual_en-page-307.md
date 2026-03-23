

```markdown
## 8.2.1 Overview

ESP32-C6 clocks are mainly sourced from oscillator (OSC), RC, and PLL circuit, and then processed by the dividers or selectors, which allows most functional modules to select their working clock according to their power consumption and performance requirements. Figure 8.2-1 shows the system clock structure.

## 8.2.2 Architectural Overview

![Figure 8.2-1. System Clock](image)

**Note:**
The AUTODIV in the figure will divide 480 MHz PLL_CLK into 160 MHz clock by hardware control only when the MUX before selects PLL_CLK. If the MUX before selects RC_FAST_CLK or XTAL_CLK, AUTODIV will not divide the clock frequency.

## 8.2.3 Features

ESP32-C6 clock sources as shown on the left side of Figure 8.2-1 can be classified into two types depending on their frequencies:
```