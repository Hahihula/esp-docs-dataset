

```markdown
## 14.3.2 Super Watchdog Controller

### 14.3.2.1 Structure

![Figure 14.3-1. Super Watchdog Controller Structure](image_path_if_available)

### 14.3.2.2 Workflow

In normal state:

* SWD controller receives feed request from SWD.
* SWD controller can send an interrupt to main CPU.
* Main CPU can feed SWD directly by setting `RTC_WDT_SWWD_FEED`.
* When trying to feed SWD, CPU needs to disable SWD controller's write protection by writing `0x50D83AA1` to `RTC_WDT_SWWD_WKEY`. This prevents SWD from being fed by mistake when the system is operating in sub-optimal state.
* If setting `RTC_WDT_SWWD_AUTO_FEED_EN` to 1, SWD controller can also feed SWD itself without any interaction with CPU.

After reset:

* Check `RTC_CLKRST_RESET_CAUSE[4:0]` for the cause of CPU reset.  
  If `RTC_CLKRST_RESET_CAUSE[4:0] == 0x12`, it indicates that the cause is SWD reset.
* Set `RTC_WDT_SWWD_RST_FLAG_CLR` to clear the SWD reset flag.

## 14.4 Interrupts

For watchdog timer interrupts, please refer to Section 13.3.7 Interrupts in Chapter 13 Timer Group (TIMG).
```