

```markdown
Chapter 15 System Timer

GoBack

15.3 System Timer Structure

The timer consists of two counters: UNIT0 and UNIT1. The count values can be monitored by three comparators, COMPO, COMP1, and COMP2. See the timer block diagram in Figure 15.3-1.

Figure 15.3-1. System Timer Structure

15.4 Clock Source Selection

The counters and comparators use XTAL_CLK or RC_FAST_CLK as the clock sources. The clock source can be selected by configuring field HP_SYS_CLKRST_REG_SYSTIMER_CLK_SRC_SEL in register HP_SYS_CLKRST_PERI_CLK_CTRL21_REG. After XTAL_CLK is scaled by 2.5, a counter clock signal CNT_CLK clock is generated with a frequency of fXTAL_CLK/2.5. The average clock frequency of CNT_CLK is 16 MHz, as shown in Figure 15.5-1. The timer counter is incremented by 1/16 µs on each CNT_CLK cycle.

Software operation such as configuring registers is clocked by APB_CLK. For more information about APB_CLK, see Chapter 10 Reset and Clock.

The following two bits of system registers are also used to control the system timer:

- Set HP_SYS_CLKRST_REG_SYSTIMER_APB_CLK_EN in register HP_SYS_CLKRST_SOC_CLK_CTRL2_REG to enable APB_CLK signal to the system timer.
- Set HP_SYS_CLKRST_REG_RST_EN_SYSTIMER in register HP_SYS_CLKRST_HP_RST_EN1_REG to reset the system timer.

Note that if the timer is reset, its registers will be restored to their default values. For more information, please refer to Chapter 10 Reset and Clock.
```