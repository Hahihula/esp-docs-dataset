

```markdown
Chapter 10 System Timer (SYSTIMER)

GoBack

• Software configuring the reference count value. For example, the system timer is able to load back the sleep time recorded by the RTC timer via software after Light-sleep
• Can be configured to stall or continue running when CPU stalls or enters on-chip-debugging mode

10.3 Clock Source Selection

The counters and comparators are driven using XTAL_CLK. After scaled by a fractional divider, a fXTAL_CLK/3 clock is generated in one count cycle and a fXTAL_CLK/2 clock in another count cycle. The average clock frequency is fXTAL_CLK / 2.5, which is 16 MHz, i.e. the CNT_CLK in Figure 10.4-1. The timer counting is incremented by 1/16 µs on each CNT_CLK cycle.

Software operation such as configuring registers is clocked by APB_CLK. For more information about APB_CLK, see Chapter 6 Reset and Clock.

The following two bits of system registers are also used to control the system timer:
• SYSTEM_SYSTIMER_CLK_EN in register SYSTEM_PERIP_CLK_ENO_REG: enable APB_CLK signal to system timer.
• SYSTEM_SYSTIMER_RST in register SYSTEM_PERIP_RST_ENO_REG: reset system timer.

Note that if the timer is reset, its registers will be restored to their default values. For more information, please refer to Table Peripheral Clock Gating and Reset in Chapter 16 System Registers (SYSREG).

10.4 Functional Description

Figure 10.4-1 shows the procedure to generate alarm in system timer. In this process, one timer counter and one timer comparator are used. An alarm interrupt will be generated accordingly based on the comparison result in comparator.

10.4.1 Counter

The system timer has two 52-bit timer counters, shown as UNITn (n = 0 or 1). Their counting clock source is a 16 MHz clock, i.e. CNT_CLK. Whether UNITn works or not is controlled by two bits in register SYSTIMER_CONF_REG:

Figure 10.4-1. System Timer Alarm Generation
```