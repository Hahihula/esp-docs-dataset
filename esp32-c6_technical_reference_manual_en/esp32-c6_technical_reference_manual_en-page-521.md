

```markdown
- Timer value reload — Auto-reload at alarm or software-controlled instant reload
- RTC slow clock RTC_SLOW_CLK frequency calculation
- Level interrupt generation
- Support several ETM tasks and events

## 14.3 Functional Description

Figure 14.3-1 is a diagram of timer TO in a timer group. TO contains a 16-bit integer divider as a prescaler, a timer-based counter and a comparator for alarm generation.

### 14.3.1 16-bit Prescaler and Clock Selection

Take the TO in timer group O as an example:

- The timer can select its clock source by setting the `PCR_TGO_TIMER_CLK_SEL` field of the `PCRTIMERGROUPOTIMERCLK_CONF_REG` register. When the field is 0, XTAL_CLK is selected; when the field is 1, PLL_F80M_CLK is selected and when the field is 2, RC_FAST_CLK is selected.
- The selected clock can be switched on by setting `PCR_TGO_TIMER_CLK_EN` field of the `PCRTIMERGROUPOTIMERCLK_CONF_REG` register to 1 and switched off by setting it to 0. The clock is then divided by a 16-bit prescaler to generate the time-base counter clock (TB_CLK) used by the time-base counter. The divisor of the prescaler can be configured through the `TIMG_TO_DIVIDER` field.

`TIMG_TO_DIVIDER` field can be configured as 0 ~ 65535 for a divisor range of 2 ~ 65536. To be more specific, when `TIMG_TO_DIVIDER` is configured as:

- 0: the divisor is 65536
- 1: the divisor is 2
- 2: the divisor is also 2
- 3 ~ 65525: the divisor is 3 ~ 65535

To modify the 16-bit prescaler, please first configure the `TIMG_TO_DIVIDER` field, and then set `TIMG_TO_DIVCNT_RST` to 1. Meanwhile, the timer must be disabled (i.e. `TIMG_TO_EN` should be cleared). Otherwise, the result can be unpredictable.
```