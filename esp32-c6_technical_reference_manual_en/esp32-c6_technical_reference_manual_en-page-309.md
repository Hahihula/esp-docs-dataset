

```markdown
| Clock                  | Source                     | Frequency                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------|
| HP_ROOT_CLK¹           | PLL_CLK<br>XTAL_CLK<br>RC_FAST_CLK | 480 MHz, will be divided to 160 MHz clock by hardware<br>40 MHz<br>17.5 MHz   |
| CPU_CLK²               | PLL_CLK<br>Low-speed clock source³ | f_HP_ROOT_CLK / (PCR_CPU_HS_DIV_NUM + 1)<br>f_HP_ROOT_CLK / (PCR_CPU_LS_DIV_NUM + 1) |
| AHB_CLK⁴               | PLL_CLK<br>Low-speed clock source     | f_HP_ROOT_CLK / (PCR_AHB_HS_DIV_NUM + 1)<br>f_HP_ROOT_CLK / (PCR_AHB_LS_DIV_NUM + 1) |

¹ HP_ROOT_CLK: the clock source of CPU_CLK, AHB_CLK and APB_CLK. If the clock source is PLL_CLK, it will be divided into 160 MHz clock by hardware after selecting the source.
² CPU_CLK frequency must be an integer multiple of AHB_CLK frequency.
³ XTAL_CLK and RC_FAST_CLK
⁴ AHB_CLK frequency can not exceed 40 MHz.

The available divider values for CPU_CLK and AHB_CLK are as follows:

*   `PCR_CPU_HS_DIV_NUM`: 0, 1, 3
*   `PCR_CPU_LS_DIV_NUM`: 0, 1, 3, 7, 15, 31
*   `PCR_AHB_HS_DIV_NUM`: 3, 7, 15
*   `PCR_AHB_LS_DIV_NUM`: 0, 1, 3, 7, 15, 31

As shown in 8.2-1, to generate APB_CLK, AHB_CLK might be divided twice. The first division is compulsory. That is, AHB_CLK is always divided by the divisor (`PCR_APB_DIV_NUM + 1`). The second division (also called automatic frequency reduction) is optional. When there is no request from the host in the chip to access peripheral registers, AHB_CLK will be further divided by `APB_DECREASE_DIV_NUM + 1`. If the host initiates a request to access peripheral registers, APB_CLK will be restored to the frequency after the first division.

Note that the chip’s performance will degrade due to the automatic frequency reduction. This function can be disabled (already disabled by default) by configuring `APB_DECREASE_DIV_NUM` to 0.
```

```markdown
## 8.2.4.2 LP System Clock

The LP system can operate when most other clocks are disabled. LP system clocks include LP_SLOW_CLK and LP_FAST_CLK.

The clock sources for LP_SLOW_CLK and LP_FAST_CLK are low-frequency clocks:

*   **LP_SLOW_CLK** can be derived from:
    -   RC_SLOW_CLK
    -   XTAL32K_CLK
    -   OSC_SLOW_CLK

*   **LP_FAST_CLK** can be derived from:
    -   20 MHz XTAL_D2_CLK, which is XTAL_CLK divided by 2
    -   RC_FAST_CLK
```