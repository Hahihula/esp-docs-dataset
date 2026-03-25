

```markdown
Chapter 12 System Timer (SYSTIMER)

- Three comparators generating three independent interrupts based on configured alarm value (t) or alarm period ($\hat{t}$)
- Software configuring the reference count value. For example, the system timer is able to load back the sleep time recorded by RTC timer via software after Light-sleep
- Able to stall or continue running when CPU stalls or enters on-chip-debugging mode
- Alarm for Event Task Matrix (ETM) event

## 12.3 Clock Source Selection

The counters and comparators use XTAL_CLK or RC_FAST_CLK as clock source. The clock source can be selected by configuring field `PCR_SYSTIMER_FUNC_CLK_SEL` in register `PCR_SYSTIMER_FUNC_CLK_CONF_REG`. After XTAL_CLK is divided by 2, a $f_{XTAL\_CLK}/2$ clock is generated in one count cycle, which is 16 MHz, i.e., the CNT_CLK in Figure 12.4-1. The timer counter is incremented by $1/16\ \mu s$ on each CNT_CLK cycle. If RC_FAST_CLK is selected as the clock source, then it will not be divided and will directly connect to the SYSTIMER controller.

Software operation such as configuring registers is clocked by APB_CLK. For more information about APB_CLK, see Chapter 7 Reset and Clock.

The following two bits of system registers are also used to control the system timer:

- Set `PCR_SYSTIMER_CLK_EN` in register `PCR_SYSTIMER_CONF_REG` to enable APB_CLK signal to the system timer.
- Set `PCR_SYSTIMER_RST_EN` in register `PCR_SYSTIMER_CONF_REG` to reset the system timer.

Note that if the timer is reset, its registers will be restored to their default values. For more information, please refer to Chapter 7 Reset and Clock.

## 12.4 Functional Description

Figure 12.4-1. System Timer Alarm Generation
```