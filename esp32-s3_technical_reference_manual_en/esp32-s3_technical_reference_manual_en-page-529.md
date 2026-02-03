**Chapter Title:**
Chapter 7 Reset and Clock

**GoBack Link:** (Hyperlink)

---

**Section Heading:**

7.2 Clock

**Subsection Heading:**

7.2.1 Overview

**Body Text:**
ESP32-S3 clocks are mainly sourced from oscillator (OSC), RC, and PLL circuit, and then processed by the dividers/selectors, which allows most functional modules to select their working clock according to their power consumption and performance requirements. Figure 7.2-1 shows the system clock structure.

**Image Description:**
Figure 7.2-1 Clock Structure

---

**Subsection Heading:**

7.2.2 Architectural Overview

---

**Subsection Heading:**

7.2.3 Features

**Body Text:**
ESP32-S3 clocks can be classified in two types depending on their frequencies:

- High speed clocks for devices working at a higher frequency, such as CPU and digital peripherals
  - PLL_CLK (320 MHz or 480 MHz): internal PLL clock
  - XTAL_CLK (40 MHz): external crystal clock

- Slow speed clocks for low-power devices, such as RTC module and low-power peripherals.

**Footer:**
Espressif Systems  
529  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)