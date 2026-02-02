**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack**

**Subtitle:**
Register 6.53. RTCIO_TOUCH_PADn_REG

**Body Text with Code Blocks and Descriptions:**

Continued from the previous page...

- **RTCIO TOUCH PADn SLEEP_ENABLE (SLP_SEL = 1):**
  - `1`: Enabled
  - `0`: Disabled
  - Accessible via `(R/W)`

- **RTCIO_TOUCH_PADn_SLP_OE (Output enable of the pin in sleep mode [SLPSEL = 1]):**
  - `1`: Enabled
  - `0`: Disabled
  - Accessible via `(R/W)`

- **RTCIO TOUCH PADn FUNCTION ENABLE (normal working mode [SLPSEL = 0]):**
  - `1`: Enabled
  - `0`: Disabled
  - Accessible via `(R/W)`

- **RTCIO_TOUCH_PADn_TO_GPIO:**
  - Controls the routing of touch pin input signals to IO_MUX.
  - `1`: The input signal from the touch pin is routed to IO_MUX through analog function.
  - `0`: The input signal from the touch pin is routed to IO_MUX through digital function.
  - Accessible via `(R/W)`

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback