

```markdown
- Various dedicated methods for software to feed SWD, which enables SWD to monitor the working state of the whole operating system

## 14.3.2 Super Watchdog Controller

### 14.3.2.1 Structure

![Figure 14.3-1. Super Watchdog Controller Structure](image)

### 14.3.2.2 Workflow

In normal state:

- SWD controller receives feed request from SWD.
- SWD controller sends an interrupt to HP CPU.
- HP CPU feeds SWD directly by setting `RTC_WDT_SWD_FEED`.

- When trying to feed SWD, CPU needs to disable SWD controller's write protection by writing `0x50D83AA1` to `RTC_WDT_SWD_WKEY`. This prevents SWD from being fed by mistake when the system is operating in sub-optimal state.

- If setting `RTC_WDT_SWD_AUTO_FEED_EN` to 1, SWD controller can also receive interrupts from the SWD for feeding the watchdog itself without any interaction with CPU.

After reset:

- Check `LP_CLKRST_RESET_CAUSE[4:0]` for the cause of CPU reset.  
  If `LP_CLKRST_RESET_CAUSE[4:0] == 0x12`, it indicates that the cause is SWD reset.

- Set `RTC_WDT_SWD_RST_FLAG_CLR` to clear the SWD reset flag.
```