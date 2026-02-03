**Chapter Title:**
Chapter 7 Reset and Clock

**GoBack Link:** GoBack

**Section Heading: APB_CLK**

**Body Text:**
APB_CLK frequency is determined by the clock source of CPU_CLK as shown in Table **7.2-4**.

**Table Caption (Table 7.2-4): APB_CLK Frequency**
| CPU_CLK Source | APB_CLK Frequency |
|------------------|--------------------|
| PLL_CLK          | 80 MHz             |
| XTAL_CLK         | CPU_CLK            |
| RC_FAST_CLK      | CPU_CLK            |

**Section Heading: CRYPTO_PWM_CLK**

**Body Text:**
The frequency of CRYPTO_PWM_CLK is determined by the CPU_CLK source, as shown in Table **7.2-5**.

**Table Caption (Table 7.2-5): CRYPTO_PWM_CLK Frequency**
| CPU_CLK Source | CRYPTO_PWM_CLK Frequency |
|------------------|--------------------|
| PLL_CLK          | 160 MHz            |
| XTAL_CLK         | CPU_CLK            |
| RC_FAST_CLK      | CPU_CLK            |

**Subsection: PLL_F160M_CLK**

**Body Text:**
PLL_F160M_CLK is divided from PLL_CLK according to current PLL frequency, so the frequency of PLL_F160M_CLK is always 160 Mhz.

**Subsection: PLL_D2_CLK**

**Body Text:**
PLL_D2_CLK is divided from PLL_CLK according to current PLL frequency.

**Subsection: LEDC_CLK**

**Body Text:**
LEDC module uses RC_FAST_CLK as clock source when APB_CLK is disabled. In other words, when the system is in low-power mode, most peripherals will be halted (APB_CLK is turned off), but LEDC can work normally via RC_FAST_CLK.

**Subsection 7.2.4.3 Wi-Fi and Bluetooth LE Clock**

**Body Text:**
Wi-Fi and Bluetooth LE can work only when CPU_CLK uses PLL_CLK as its clock source. Suspending PLL_CLK requires that Wi-Fi and Bluetooth LE has entered low-power mode first.
LOW_POWER_CLK uses XTAL32K_CLK, XTAL_CLK, RC_FAST_CLK or RTC_SLOWW_CLK (the low clock selected by RTC) as its clock source for Wi-Fi and Bluetooth LE in low-power mode.

**Subsection 7.2.4.4 RTC Clock**

**Body Text:**
The clock sources for RTC_SLOWW_CLK and RTC_FAST_CLK are low-frequency clocks. RTC module can operate when most other clocks are stopped.
RTC_SLOWW_CLK is derived from RC_SLOWW_CLK, XTAL32K_CLK or RC_FASTW_CLK and used to clock Power Management module. RTC_FASTW_CLK is used to clock On-chip Sensor module. It can be sourced from a divided XTAL_CLK or from RC_FASTW_CLK.

**Footer:**
Espressif Systems
533 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback