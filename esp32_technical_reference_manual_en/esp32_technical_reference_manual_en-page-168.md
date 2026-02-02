**Chapter Title:**
- Chapter 7 Reset and Clock

**Section Header:**
- GoBack (Link)

**Subsection Heading with Numbered Section Reference:**
- **7.2.3 CPU Clock**

**Body Text:**
As Figure 7.2-1 shows, CPU_CLK is the master clock for both CPU cores. CPU_CLK clock can be as high as 240 MHz when the CPU is in high performance mode. Alternatively, the CPU can run at lower frequencies to reduce power consumption.

The CPU_CLK source code is determined by the RTC_CNTL_SOC_CLK_SEL register. PLL_CLK, APLL_CLK, RC_FAST_CLK, and XTL_CLK can be set as the CPU_CLK source; see Table 7.2-1 and 7.2-2.

**Table Title:**
- **Table 7.2-1. CPU_CLK Source**

| RTC_CNTL_SOC_CLK_SEL Value | Clock Source |
| --- | --- |
| O | XTL_CLK |
| 1 | PLL_CLK |
| 2 | RC_FAST_CLK |
| 3 | APLL_CLK |

**Subsection Heading with Numbered Section Reference:**
- **7.2.4 Peripheral Clock**

**Body Text:**
Peripheral clocks include APB_CLK, REF_TICK, LEDC_SCLK, APLL_CLK, and PLL_F160M_CLK.

Table 7.2-3 shows which clocks can be used by which peripherals.

**Table Title:**
- **Table 7.2-2. CPU_CLK Derivation**

| Clock Source | *SEL_0* | *SEL_1* | CPU Clock Frequency |
| --- | --- | --- | --- |
| XTL_CLK | O | - | CPU_CLK = XTAL_CLK / (SYSCON_PRE_DIV_CNT+1) |
| PLL_CLK (320 MHz) | 1 | 0 | CPU_CLK = PLL_CLK / 4 |
| | 1 | 1 | CPU_CLK frequency is 80 MHz |
| | 1 | - | CPU_CLK = PLL_CLK / 2 |
| | 1 | 1 | CPU_CLK frequency is 160 MHz |
| PLL_CLK (480 MHz) | 1 | 2 | CPU_CLK = PLL_CLK / 2 |
| RC_FAST_CLK | 2 | - | CPU_CLK = RC_FAST_CLK / (SYSCON_PRE_DIV_CNT+1) |
| APLL_CLK | 3 | O | CPU_CLK = APLL_CLK / 4 |
| APB_CLK | 3 | 1 | CPU_CLK = APLL_CLK / 2 |

**Footnotes:**
- *SEL_0: The value of register RTC_CNTL_SOC_CLK_SEL
- *SEL_1: The value of register CPUIUPERIOD_SEL

**Table Title:**
- **Table 7.2-3. Peripheral Clock Usage**

| Peripherals | APB_CLK | REF_TICK | LEDC_SCLK | APLL_CLK | PLL_F160M_CLK |
| --- | --- | --- | --- | --- | --- |
| EMAC | Y | N | N | Y | N |
| TIMG | Y | N | N | N | N |
| I2S | Y | N | N | Y | Y |
| UART | Y | - | N | N | N |

**Footer:**
- Espressif Systems
- ESP32 TRM (Version 5.6)
- Page number: 168

**Action Links:**
- Submit Documentation Feedback