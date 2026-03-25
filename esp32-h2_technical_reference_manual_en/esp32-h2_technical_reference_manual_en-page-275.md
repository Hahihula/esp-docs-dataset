

```markdown
| Clock                  | Source                          | Frequency                     |
|------------------------|----------------------------------|-------------------------------|
|                        | PLL_F96M_CLK                    | 96 MHz                        |
| HP_ROOT_CLK            | PLL_F64M_CLK                    | 64 MHz                        |
|                        | XTAL_CLK                        | 32 MHz                        |
|                        | RC_FAST_CLK                     | 8 MHz                         |
| CPU_CLK¹               | HP_ROOT_CLK                     | f_HP_ROOT_CLK/(PCR_CPU_DIV_NUM+1) |
| AHB_CLK²               | HP_ROOT_CLK                     | f_HP_ROOT_CLK/(PCR_AHB_DIV_NUM+1) |

¹ CPU_CLK frequency must be larger than or equal to AHB frequency, and must be an integer multiple of AHB_CLK frequency.
² AHB_CLK frequency can not exceed 32 MHz.

Note:
When selecting the clock source of HP_ROOT_CLK, or configuring the clock divisor for CPU_CLK and AHB_CLK, please also set `PCR_BUS_CLOCK_UPDATE` to apply the new configuration, and read `PCR_BUS_CLOCK_UPDATE` to see if new configuration takes effect.
```

As shown in 7.2-1, to generate APB_CLK, AHB_CLK might be divided twice. The first division is compulsory. That is, AHB_CLK is always divided by the divisor (PCR_APB_DIV_NUM + 1). The second division (also called automatic frequency reduction) is optional. When there is no request from the host in the chip to access peripheral registers, AHB_CLK will be further divided by (APB_DECREASE_DIV_NUM + 1) to lower power consumption. If the host initiates a request to access peripheral registers, APB_CLK will be restored to the frequency after the first division.

Note that the chip's performance will degrade due to the automatic frequency reduction. This function can be disabled (already disabled by default) by configuring `APB_DECREASE_DIV_NUM` to 0.

### 7.2.4.2 LP System Clock

The LP system can operate when most other clocks are disabled. LP system clocks include LP_SLOW_CLK and LP_FAST_CLK.

The clock sources for LP_SLOW_CLK and LP_FAST_CLK are low-frequency clocks:

*   **LP_SLOW_CLK** can be derived from:
    *   RC_SLOW_CLK
    *   XTAL32K_CLK
    *   OSC_SLOW_CLK

*   **LP_FAST_CLK** can be derived from:
    *   16 MHz XTAL_D2_CLK, which is XTAL_CLK divided by 2
    *   RC_FAST_CLK
    *   PLL_LP_CLK
```