

```markdown
- Timer value reload — Auto-reload at alarm or software-controlled instant reload
- Frequency calculation of slow clock for timer group 0
- Level interrupt generation
- Support several ETM tasks and events


## 15.3 Architectural Overview

Figure 15.3-1 is a diagram of timer TO in a timer group. TO contains a 16-bit integer divider as a prescaler, a timer-based counter, and a comparator for alarm generation.

## 15.4 Functional Description

### 15.4.1 16-bit Prescaler and Clock Selection

Take the TO in timer group 0 as an example:

- The timer can select its clock source by setting the `PCR_TGO_TIMER_CLK_SEL` field of the `PCR_TIMERGROUPOTIMER_CLK_CONF_REG` register. When the field is 0, CLKO is selected, which indicates XTAL_CLK; when the field is 1, CLK1 is selected, which indicates RC_FAST_CLK; when the field is 2, CLK2 is selected, which indicates PLL_F8OM_CLK.

- The selected clock can be switched on by setting `PCR_TGO_TIMER_CLK_EN` field of the `PCR_TIMERGROUPOTIMER_CLK_CONF_REG` register to 1 and switched off by setting it to 0. This field is indicated as TIMER_CLK_EN in Figure 15.3-1. The clock is then divided by a 16-bit prescaler to generate the time-base counter clock (TB_CLK) used by the time-base counter. The divisor of the prescaler can be configured through the `TIMG_TO_DIVIDER` field.

`TIMG_TO_DIVIDER` field can be configured as 0 ~ 65535 for a divisor range of 2 ~ 65536. To be more specific, when `TIMG_TO_DIVIDER` is configured as:

- 0: the divisor is 65536
- 1: the divisor is 2
- 2: the divisor is also 2
- 3 ~ 65525: the divisor is 3 ~ 65535
```