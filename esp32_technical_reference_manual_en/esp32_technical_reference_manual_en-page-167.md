**Title: Chapter 7 Reset and Clock**

---

**Diagram Title:** CLK MANAGEMENT

- **Components in Diagram (from top to bottom, left to right):**
  - PLL_CLK -> DIVA -> CPU_CLK -> CPU
  - APLL_CLK -> DIVB -> APB_CLK -> WIFI
  - RC_FAST_CLK -> MUX -> REF_GEN -> REF_TICK -> BT
  - XTAL_CLK -> LP_CLK_GEN -> LEDC_SCLK -> Peri
  - (Other components and connections are shown in the diagram)

---

**Figure Caption:**
- Figure 7.2-1. System Clock

---

**Subtitle:** 7.2.2 Clock Source

**Body Text:**

The ESP32 can use an external crystal oscillator, an internal PLL or an oscillating circuit as a clock source.
Specifically, the clock sources available are:

- **High Speed Clocks**
  - PLL_CLK is an internal PLL clock with a frequency of 320 MHz or 480 MHz.

- **XTL_CLK** is a clock signal generated using an external crystal with a frequency range of 2 ~ 40 MHz.
  
- **Low Power Clocks**
  - XTL32K_CLK is a clock generated using an external crystal with a frequency of 32 KHz.
  - RC_FAST_CLK is an internal clock with a default frequency of 8 MHz. This frequency is adjustable.

- **RC_FAST_DIV_CLK** is divided from RC_FAST_CLK. Its frequency is (RC_FAST_CLK / 256). With the default RC_FAST_CLK frequency of 8 MHz, this clock runs at 31.250 KHz.
  
- **RC_SLOW_CLK** is an internal low power clock with a default frequency of 150 KHz. This frequency is adjustable.

---

**Subsection:** Audio Clock

---

**Footer:**
- Page number and document version information:
  - "Espressif Systems"
  - "ESP32 TRM (Version 5.6)"
  - "Submit Documentation Feedback"