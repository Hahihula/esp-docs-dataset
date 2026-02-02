**Chapter Title:**
Chapter 7 Reset and Clock

**Table Header:**
Table 7-26. LEDC_SCLK Derivation

| LDC_APB_CLK_SEL Value | LEDC_SCLK Source |
|------------------------|------------------|
| 0                      | RC_FAST_CLK      |
| 1                      | APB_CLK          |

**Section Title and Subsections with Content:**

#### 7.2.4.4 APLL_SCLK Source
The APLL_CLK is sourced from PLL_CLK, with its output frequency configured using the APLL configuration registers.

#### 7.2.4.5 PLL_F160M_CLK Source
PLL_F160M_CLK is divided from PLL_CLK by automatically adjusting the clock division and its frequency is always 160 MHz.

#### 7.2.4.6 Clock Source Considerations
Most peripherals will operate using the APB_CLK frequency as a reference. When this frequency changes, the peripherals will need to update their clock configuration to operate at the same frequency after the change. Peripherals accessing REF_TICK can continue operating normally when switching clock sources, without changing clock source. Please see Table 7-23 for details.

The LED PWM module can use RC_FAST_CLK as a clock source when APB_CLK is disabled. In other words, when the system is in low-power consumption mode (see Chapter [9 Low-Power Management](#)), normal peripherals will be halted (APB_CLK is turned off), but the LED PWM can work normally via RC_FAST_CLK.

#### 7.2.5 Wi-Fi BT Clock
Wi-Fi and BT can only operate if APB_CLK uses PLL_CLK as its clock source. Suspending PLL_CLK requires Wi-Fi and BT to both have entered low-power consumption mode first.
For LOW_POWER_CLK, one of RC_SLOW_CLK, RTC_SLOW_CLK, RC_FAST_CLK or XTL_CLK can be selected as the low-power consumption mode clock source for Wi-Fi and BT.

#### 7.2.6 RTC Clock
The clock sources of RTC_SLOW_CLK and RTC_FAST_CLK are low-frequency clocks. The RTC module can operate when most other clocks are stopped.
RTC_SLOW_CLK is used to clock the Power Management module. It can be sourced from RC_SLOW_CLK, XTL32K_CLK or RC_FAST_DIV_CLK.
RTC_FAST_CLK is used to clock the On-chip Sensor module. It can be sourced from a divided XTL_CLK or from RC_FAST_CLK.

#### 7.2.7 Audio PLL
The operation of audio and other time-critical data-transfer applications requires highly-configurable, low-jitter, and accurate clock sources. The clock sources derived from system clocks that serve digital peripherals may

**Footer:**
Espressif Systems  
170  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)