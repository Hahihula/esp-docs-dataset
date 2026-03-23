

```markdown
Chapter 12 Watchdog Timers (WDT)

GoBack

12.3.2.1 Structure

Figure 12.3-1. Super Watchdog Controller Structure

ANALOG
Super Watchdog
Swd_feed
Swd_clr_flag
Swd_intr
Swd_rst_flag
Swd_rstb
RTC
SWD Controller
RTC REG
PERIBUS
DIGITAL
CPU
INTERRUPT

12.3.2.2 Workflow

In normal state:

- SWD controller receives feed request from SWD.
- SWD controller can send an interrupt to main CPU.
- Main CPU can feed SWD directly by setting RTC_CNTL_SWD_FEED.
- When trying to feed SWD, CPU needs to disable SWD controller's write protection by writing 0x8F1D312A to RTC_CNTL_SWD_WKEY. This prevents SWD from being fed by mistake when the system is operating in sub-optimal state.
- If setting RTC_CNTL_SWD_AUTO_FEED_EN to 1, SWD controller can also feed SWD itself without any interaction with CPU.

After reset:

- Check RTC_CNTL_RESET_CAUSE_PROCPU[5:0] for the cause of CPU reset.
  If RTC_CNTL_RESET_CAUSE_PROCPU[5:0] == 0x12, it indicates that the cause is SWD reset.
- Set RTC_CNTL_SWD_RST_FLAG_CLR to clear the SWD reset flag.

12.4 Interrupts

For watchdog timer interrupts, please refer to Section 11.2.6 Interrupts in Chapter 11 Timer Group (TIMG).
```