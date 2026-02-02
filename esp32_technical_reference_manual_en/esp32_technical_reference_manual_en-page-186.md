**Title: Chapter 9 Low-Power Management (RTC_CNTL)**

---

### Diagram Description:
The diagram is a block diagram titled "Figure 9-35. RTC Structure". It illustrates the flow of control between various components in low-power management, including Sleep Controller, Analog Power Controller, Digital Power Controller with Wi-Fi and Core sections labeled as ROM / RAM, Protection Timer, Coprocessor done, Touch Timer, ULP-coprocessor, Wakeup Controller, and various wake-up signals to different timers (EXT0, EXT1, Digital GPIO, RTC GPIO, SDIO, MAC, BT, UART0).

---

### Subtitle: 9.3.7 Low-Power Clocks

**Body Text:**
In the low-power mode, the 40 MHz crystal and PLL are usually powered down to save power. But clocks are needed for the chip to remain active in the low-power mode.

For the RTC core, there are five possible clock sources:
- external low-speed (32.768 kHz) crystal clock XTL32K_CLK,
- external high-speed (2 MHz ~ 40 MHz) crystal clock XTAL_DIV_CLK,
- internal RC oscillator RC_SLOW_CLK (typically about 150 kHz and adjustable),
- internal 8-MHz oscillator RC_FAST_CLK, and
- internal 31.25-kHz clock RC_FAST_DIV_CLK (derived from the internal 8-MHz oscillator divided by 256).

With these clocks, RTC_FAST_CLK and RTC_SLOW_CLK is derived. By default, RTC_FAST_CLK is RC_FAST_CLK while RTC_SLOW_CLK is RC_SLOW_CLK.

---

**Footer:**
Espressif Systems  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback