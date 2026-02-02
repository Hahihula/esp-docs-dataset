**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header with Backlink:**
GoBack

**Body Text:**
When configured as RTC GPIOs, the output pins can still retain the output level value when the chip is in Deep-sleep mode, and the input pins can wake up the chip from Deep-sleep.

**Subsection Title (with reference):**
Section 6.11 has a list of RTC_MUX pins and their functions

**Subsection Header:**
6.5.2 Analog Function Description

**Body Text under Subsection:**
The RTC function and analog function of RTC_GPIOs can only be selected one at a time. For the RTC_GPIO8 to RTC_GPIO17 pins, their analog outputs can be directed to the IO MUX, controlled by the RTC_IO_TOUCH_PADn/m_TO_GPIO bit. If the bit is set to 1, the analog output is enabled, allowing the signal to be routed to IO MUX through analog function. On the other hand, if the bit is set to 0, the input signal from the pin is output to IO MUX through digital function.

**Subsection Header:**
6.6 Light-sleep Mode Pin Functions

**Body Text under Subsection:**
Pins can have different functions when the ESP32 is in Light-sleep mode. If the SLP_SEL bit in the IO MUX register for a GPIO pin is set to 1, a different set of registers is used to control the pin when the ESP32 is in Light-sleep mode:

**Table Title:**
Table 6.6-1. IO_MUX Light-sleep Pin Function Registers

| IO_MUX Function | Normal Execution (OR SLP_SEL = 0) | Light-sleep Mode (AND SLP_SEL = 1) |
|------------------|-------------------------------------|--------------------------------------|
| Output Drive Strength | FUN_DRV | MCU_DRV |
| Pull-up Resistor | FUN_WPU | MCU_WPU |
| Pull-down Resistor | FUN_WPD | MCU_WPD |
| Output Enable | (From GPIO Matrix _OEN field) | MCU_OE |

**Body Text under Table:**
If SLP_SEL is set to 0, the pin functions remain the same in both normal execution and Light-sleep mode.

**Subsection Header:**
6.7 pin Hold Feature

**Body Text under Subsection:**
Each IO pin (including the RTC pins) has an individual hold function controlled by a RTC register. When the pin is set to hold, the state is latched at that moment and will not change no matter how the internal signals change or how the IO MUX configuration or GPIO configuration is modified. Users can use the hold function for the pins to retain the pin state through a core reset triggered by watchdog time-out or Deep-sleep events.

The Hold state of each pin is controlled by the result of OR operation of the pin’s Hold enable signal and the global Hold enable signal.
- **Bullet Point:**
  - Digital Pins (GPIO18 ~ GPIO19, GPIO21 ~ GPIO23, GPIO25 ~ GPIO27, GPIO32 ~ GPIO39)
    - RTCIO_DIG_PAD_HOLD_REG[n], controls the Hold enable signal of each digital pin. See Table 6.13-1 for the bit mapping for the pins.
    - RTC_CNTL_DG_PAD FORCE_HOLD, controls the global Hold signal of all digital pins.

**Footer:**
Espressif Systems
Page number indicator (121)
ESP32 TRM (Version 5.6)