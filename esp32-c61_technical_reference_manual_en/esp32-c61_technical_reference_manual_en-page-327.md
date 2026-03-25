

```markdown
| PCR_SOC_CLK_SEL | CPU Clock Source |
|-----------------|------------------|
| 0               | XTAL_CLK         |
| 1               | RC_FAST_CLK      |
| 2               | PLL_F160M_CLK    |

Table 7.2-2. Frequency of CPU_CLK, AHB_CLK and HP_ROOT_CLK

<table><thead><tr><th>Clock</th><th>Source</th><th>Frequency</th></tr></thead><tbody><tr><td rowspan="3">HP_ROOT_CLK</td><td>PLL_F160M_CLK</td><td>160 MHz</td></tr><tr><td>XTAL_CLK</td><td>40 MHz</td></tr><tr><td>RC_FAST_CLK</td><td>20 MHz</td></tr><tr><td>CPU_CLK<sup>1</sup></td><td>HP_ROOT_CLK</td><td>f<sub>HP_ROOT_CLK</sub> / ( PCR_CPU_DIV_NUM + 1 )</td></tr><tr><td>AHB_CLK<sup>2</sup></td><td>HP_ROOT_CLK</td><td>f<sub>HP_ROOT_CLK</sub> / ( PCR_AHB_DIV_NUM + 1 )</td></tr></tbody></table>

Note:
When selecting the clock source of HP_ROOT_CLK, or configuring the clock divisor for CPU_CLK and AHB_CLK, please also set `PCR_BUS_CLOCK_UPDATE` to apply the new configuration, and read `PCR_BUS_CLOCK_UPDATE` to see if new configuration takes effect.

As shown in 7.2-1, to generate APB_CLK, AHB_CLK might be divided twice. The first division is compulsory. That is, AHB_CLK is always divided by the divisor (PCR_APB_DIV_NUM + 1). The second division (also called automatic frequency reduction) is optional. When there is no request from the host in the chip to access peripheral registers, AHB_CLK will be further divided by (APB_DECREASE_DIV_NUM + 1) to lower power consumption. If the host initiates a request to access peripheral registers, APB_CLK will be restored to the frequency after the first division.

Note that the function of automatic frequency reduction can be disabled (already disabled by default) by configuring `APB_DECREASE_DIV_NUM` to 0.
```