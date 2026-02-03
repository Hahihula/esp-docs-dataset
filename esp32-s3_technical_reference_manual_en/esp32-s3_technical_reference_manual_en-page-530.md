**Chapter Title:**
- Chapter 7 Reset and Clock

**GoBack Link:** (Located at top right corner)

**List of Clock Sources with Descriptions:**
1. XTAL32K_CLK (32 kHz): external crystal clock
2. RC_FAST_CLK (17.5 MHz by default): internal fast RC oscillator clock with adjustable frequency
3. RC_FAST_DIV_CLK: internal fast RC oscillator clock derived from RC_FAST_CLK divided by 256
4. RC_SLOW_CLK (136 kHz by default): internal low RC oscillator clock with adjustable frequency

**Section Title:** 
- **7.2.4 Functional Description**

**Subsection Title and Content:**
- **7.2.4.1 CPU Clock**
  
  As Figure [7.2-1](#) shows, CPU_CLK is the master clock for CPUx and it can be as high as 240 MHz when CPUx works in high performance mode. Alternatively, CPUx can run at lower frequencies, such as at 2 MHz, to lower power consumption.

  Users can set PLL_CLK, RC_FAST_CLK or XTAL_CLK as CPU_CLK source by configuring register SYSTEM_SOC_CLK_SEL, see table [7.2-1](#) and table **[7.2-2](#)**.
  
**Table Titles:**
- Table *7.2-1*. CPU Clock Source
  - Columns:
    - SYSTEM_SOC_CLK_SEL Value (0 to 3)
    - CPU Clock Source

**Table Content for CPU Clock Source:**
| SYSTEM_SOC_CLK_SEL Value | CPU Clock Source |
|---------------------------|------------------|
| 0                         | XTAL_CLK         |
| 1                         | PLL_CLK          |
| 2                         | RC_FAST_CLK      |

- Table *7.2-2*. CPU Clock Frequency
  - Columns:
    - CPU Clock Source
    - SEL_0*
    - SEL_1*
    - SEL_2*
    - CPU Clock Frequency

**Table Content for CPU Clock Frequency:**
| CPU Clock Source | SEL_0* | SEL_1* | SEL_2* | CPU Clock Frequency |
|------------------|--------|--------|--------|--------------------|
| XTAL_CLK        | 0      | -      | -      | CPU_CLK = XTAL_CLK/(SYSTEM_PRE_DIV_CNT + 1) |
| PLL_CLK (480 MHz)| 1      | 1      | 0      | SYSTEM_PRE_DIV_CNT ranges from 0 ~ 1023. Default is 1 |
| PLL_CLK (480 MHz)| 1      | -      | 1      | CPU_CLK = PLL_CLK/6 |
| PLL_CLK (480 MHz)| 1      | 1      | 1      | CPU_CLK frequency is ≈ 80 MHz |
| PLL_CLK (320 MHz)| 1      | 0      | 0      | CPU_CLK = PLL_CLK/3 |
| PLL_CLK (320 MHz)| -      | 0      | 1      | CPU_CLK frequency is ≈ 160 MHz |
| PLL_CLK (480 MHz)| 1      | 0      | 1      | CPU_CLK = PLL_CLK/2 |
| PLL_CLK (320 MHz)| 1      | -      | 1      | CPU_CLK = PLL_CLK/2 |
| RC_FAST_CLK      | 2      | -      | -      | CPU_CLK = RC_FAST_CLK/(SYSTEM_PRE_DIV_CNT + 1) |

**Footnotes:**
- *The value of register SYSTEM_SOC_CLK_SEL.
- *The value of register SYSTEM_PLL_FREQ SEL.
- *The value of register SYSTEM_CPU_PERIOD_SEL.

**Footer Information:** 
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Page number and feedback link: "Submit Documentation Feedback" at the bottom right corner