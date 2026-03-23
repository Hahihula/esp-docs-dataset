

```markdown
## 6.2.4.1 CPU Clock

As Figure 6.2-1 shows, CPU_CLK is the master clock for CPU and it can be as high as 160 MHz when CPU works in high performance mode. Alternatively, CPU can run at lower frequencies, such as at 2 MHz, to lower power consumption. Users can set PLL_CLK, RC_FAST_CLK or XTAL_CLK as CPU_CLK clock source by configuring register SYSTEM_SOC_CLK_SEL, see Table 6.2-1 and Table 6.2-2. By default, the CPU clock is sourced from XTAL_CLK with a divider of 2, i.e. the CPU clock is 20 MHz.

Table 6.2-1. CPU Clock Source

| SYSTEM_SOC_CLK_SEL Value | CPU Clock Source |
|--------------------------|------------------|
| 0                        | XTAL_CLK         |
| 1                        | PLL_CLK          |
| 2                        | RC_FAST_CLK      |

Table 6.2-2. CPU Clock Frequency

| CPU Clock Source | SEL_0* | SEL_1* | SEL_2* | CPU Clock Frequency                                                                                     |
|------------------|--------|--------|--------|---------------------------------------------------------------------------------------------------------|
| XTAL_CLK         | 0      | -      | -      | CPU_CLK = XTAL_CLK/(SYSTEM_PRE_DIV_CNT + 1)<br>SYSTEM_PRE_DIV_CNT ranges from 0 ~ 1023. Default is 1     |
| PLL_CLK (480 MHz)| 1      | 1      | 0      | CPU_CLK = PLL_CLK/6<br>CPU_CLK frequency is 80 MHz                                                     |
| PLL_CLK (480 MHz)| 1      | 1      | 1      | CPU_CLK = PLL_CLK/3<br>CPU_CLK frequency is 160 MHz                                                    |
| PLL_CLK (320 MHz)| 1      | 0      | 0      | CPU_CLK = PLL_CLK/4<br>CPU_CLK frequency is 80 MHz                                                     |
| PLL_CLK (320 MHz)| 1      | 0      | 1      | CPU_CLK = PLL_CLK/2<br>CPU_CLK frequency is 160 MHz                                                    |
| RC_FAST_CLK      | 2      | -      | -      | CPU_CLK = RC_FAST_CLK/(SYSTEM_PRE_DIV_CNT + 1)<br>SYSTEM_PRE_DIV_CNT ranges from 0 ~ 1023. Default is 1 |

* The value of SYSTEM_SOC_CLK_SEL.
* The value of SYSTEM_PLL_FREQ_SEL.
* The value of SYSTEM_CPU_PERIOD_SEL.

## 6.2.4.2 Peripheral Clock

Peripheral clocks include APB_CLK, CRYPTO_CLK, PLL_F160M_CLK, LEDC_SCLK, XTAL_CLK, and RC_FAST_CLK. Table 6.2-3 shows which clock can be used by each peripheral.
```