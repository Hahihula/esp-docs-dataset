**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

**Body Text:**
To use this feature, follow the steps below:
- To maintain the pin's input/output status in Deep-sleep, set `RTCIO_DIG_PAD_HOLD_REG[n]` (`n = 0 ~ 31`) before power off. See Table **6.13-1** for the bit mapping for the pins. To disable the Hold function of each pin after the chip is woken up, clear the bits above.
- Alternatively, set `RTC_CNTL_DG_PADFORCE_HOLD` to hold the values of all digital pins, or set `RTC_CNTL_DG_PADFORCE_UNHOLD` to disable the hold function of all digital pins.

**Subsection: RTC Pins (GPIO0 ~ GPIO17)**
- `RTC_CNTL_HOLD FORCE REG[n] (n = 0 ~ 17)` controls the Hold enable signal of each RTC pin (`GPIO0 ~ GPIO17`).
- `RTC_CNTL_DG_PAD FORCE HOLD`, controls the global Hold signal of all RTC pins.

To use this feature, follow these steps below:
- To maintain the pin's input/output status in Deep-sleep, set `RTC_CNTL_DIG_PAD_HOLD_REG[n]`. `n` ranges from 0 to 17, corresponding to GPIO0 ~ GPIO17, respectively. To disable the Hold function of each pin after the chip is woken up, clear the bits above.
- Alternatively, set `RTC_CNTL_DG_PAD FORCE_HOLD` to hold the values of all RTC pins, or set `RTC_CNTL_DG_PADFORCE_UNHOLD` to disable the hold function of all RTC pins.

**Section Title: 6.8 I/O Pin Power Supplies**

**Figure Caption:** Figure **6.8-1 and 6.8-2** show the IO pin power supplies.
- The figure is a diagram labeled "Figure 6.8-1 ESP32 I/O Pin Power Sources (QFN 6*6, Top View)" showing various pins with their corresponding labels such as VDDA, LNA_IN, VDD3P3, etc.

**Footer:**
Espressif Systems
Page number: **122**
Document version: **ESP32 TRM (Version 5.6)**
Link to submit feedback or documentation is provided at the bottom of the page ("Submit Documentation Feedback").