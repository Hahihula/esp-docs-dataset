

```markdown
Chapter 12 System Timer

GoBack

## 12.3 System Timer Structure

The timer consists of two counters: UNIT0 and UNIT1. The count values can be monitored by three comparators, COMPO, COMP1, and COMP2. See the timer block diagram in Figure 12.3-1.

![Figure 12.3-1. System Timer Structure](image)

## 12.4 Clock Source Selection

The counters and comparators use XTAL_CLK or RC_FAST_CLK as the clock sources. The clock source can be selected by configuring field `PCR_SYSTIMER_FUNC_CLK_SEL` in register `PCR_SYSTIMER_FUNC_CLK_CONF_REG`. After XTAL_CLK is scaled, a counter clock signal CNT_CLK clock is generated. The average clock frequency of CNT_CLK is 16 MHz, as shown in Figure 12.5-1. The timer counter is incremented by 1/16 µs on each CNT_CLK cycle.

Software operation such as configuring registers is clocked by APB_CLK. For more information about APB_CLK, see Chapter 7 Reset and Clock.

The following two bits of system registers are also used to control the system timer:

*   Set `PCR_SYSTIMER_CLK_EN` in register `PCR_SYSTIMER_CONF_REG` to enable APB_CLK signal to the system timer.
*   Set `PCR_SYSTIMER_RST_EN` in register `PCR_SYSTIMER_CONF_REG` to reset the system timer.

Note that if the timer is reset, its registers will be restored to their default values. For more information, please refer to Chapter 7 Reset and Clock.
```