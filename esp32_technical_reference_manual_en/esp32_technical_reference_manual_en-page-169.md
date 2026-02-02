**Chapter Title:**
Chapter 7 Reset and Clock

**GoBack Link:** GoBack

**Table Section Header (with table):**

| RMT | Y   |
|-----|-----|
| LED PWM | Y    |
| PWM | N     |
| I2C | Y      |
| SPI | N       |
| PCNT | N        |
| eFuse Controller | N         |
| SDIO Slave | N          |
| SDMMC | N           |

**Subsection Title:**
7.2.4.1 APB_CLK

**Body Text:**
The APB_CLK frequency is determined by CPU_CLK source, as detailed in Table 7.2-4.

**Table Reference (with table):**

| CPU_CLK Source       | APB_CLK Frequency |
|----------------------|--------------------|
| PLL_CLK              | 80 MHz             |
| APLL_CLK            / 2   | CPU_CLK           |
| XTL_CLK             | CPU_CLK           |
| RC_FAST_CLK         | CPU_CLK           |

**Subsection Title:**
7.2.4.2 REF_TICK

**Body Text:**
REF_TICK is derived from APB_CLK. The APB_CLK frequency is determined by CPU_CLK source. The REF_TICK frequency should be fixed. When CPU_CLK source changes, users need to make sure the REF_TICK frequency remains unchanged setting a correct divider value.

Clock divider registers are shown in Table 7.2-5.

**Table Reference (with table):**

| CPU_CLK Source       | APB_CLK Frequency |
|----------------------|--------------------|
| PLL_CLK              | 80 MHz             |
| APLL_CLK            / 2   | CPU_CLK           |
| XTL_CLK             | CPU_CLK           |
| FOSC_CLK            | CPU_CLK           |

**Example Text:**
For example, when CPU_CLK source is PLL_CLK and users need to keep the REF_TICK frequency at 1 MHz,
then they should set SYSCON_PLL_TICK_NUM to 79 (0x4F) so that the REF_TICK frequency = 80 MHz / (79+1) = 1 MHz.

**Subsection Title:**
7.2.4.3 LEDC_SCLK Source

**Body Text:**
The LEDC_SCLK clock source is selected by the LEDC_APB_CLK_SEL register, as shown in Table 7.2-6.

**Footer Information:** 
Espressif Systems
ESP32 TRM (Version 5.6)
Page number at bottom center of page.
Submit Documentation Feedback link