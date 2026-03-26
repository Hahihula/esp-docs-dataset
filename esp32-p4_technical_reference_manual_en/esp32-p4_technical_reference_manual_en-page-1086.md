

```markdown
- Programmable alarm generation
- Timer value reload — Auto-reload at alarm or software-controlled instant reload
- Calculate clock frequency — Calculate the measured frequency of the clock, which can be called TIMGO_CALI_CLK, based on the crystal clock
- Level interrupt generation
- Support several ETM tasks and events

## 16.3 Functional Description

Figure 16.3-1 shows Timer Tx in timer group TIMGn. Tx contains a 16-bit integer divider as a prescaler, a timer-based counter, and a comparator for alarm generation.

![Figure 16.3-1. Timer Group Architecture](image_path)

### 16.3.1 16-bit Prescaler and Clock Selection

Take the Timer Tx in timer group TIMGn as an example:

- The timer can select its clock source by setting the HP_SYS_CLKRST_TIMERGRPn_Tx_SRC_SEL field of the HP_SYS_CLKRST_PERI_CLK_CTRL20_REG register or the HP_SYS_CLKRST_PERI_CLK_CTRL21_REG register. When the field is 0, XTAL_CLK is selected; when the field is 1, RC_FAST_CLK is selected and when the field is 2, PLL_F80M_CLK is selected.
- The selected clock can be switched on by setting HP_SYS_CLKRST_TIMERGRPn_Tx_CLK_EN field of the HP_SYS_CLKRST_PERI_CLK_CTRL20_REG register or the HP_SYS_CLKRST_PERI_CLK_CTRL21_REG register to 1 and switched off by setting it to 0. The clock is then divided by a 16-bit prescaler to generate the time-base counter clock (TB_CLK) used by the time-base counter. The divisor of the prescaler can be configured through the TIMG_Tx_DIVIDER field.

TIMG_Tx_DIVIDER field can be configured as 0 ~ 65535 for a divisor range of 2 ~ 65536. To be more specific, when TIMG_Tx_DIVIDER is configured as:

- 0: the divisor is 65536
- 1: the divisor is 2
- 2: the divisor is also 2
- 3 ~ 65535: the divisor is 3 ~ 65535
```