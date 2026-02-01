**Title: Pins**

- **Subtitle:** Pin Providing Power (either VDD3P3_CPU or VDD_SPI) is decided by eFuse bit EFUSE_PIN_POWER_SELECTION

  - Reference to ESP32-S3 Technical Reference Manual > Chapter eFuse Controller and IO_MUX_PAD_POWER_CTRLL bit.

- For ESP32-S3R8V and ESP32-S3R16V chip, as the VDD_SPI voltage has been set to 1.8 V.
  
- The default drive strengths for each pin are:
  - GPIO17 and GPIO18: 10 mA
  - GPIO19 and GPIO20: 40 mA

- All other pins: 20 mA

**Subtitle:** Column Pin Settings shows predefined settings at reset and after reset with the following abbreviations:

- IE – input enabled
- WPU – internal weak pull-up resistor enabled
- WPD – internal weak pull-down resistor enabled
- USB PU – USB pull-up resistor enabled
  
  - By default, the USB function is enabled for USB pins (i.e., GPIO19 and GPIO20), and the pin pull-up is decided by the USB pull-up. The USB pull-up is controlled by USB_SERIAL_JTAG_DP/DM_PULUP and the pull-up resistor value is controlled by USB_SERIAL_JTAG_PULLUP_VALUE.

**Subtitle:** When the USB function is disabled, USB pins are used as regular GPIOs

- The pin's internal weak pull-up and pull-down resistors are disabled by default (configurable by IO_MUXFUN_WPU/WPD).

**Note:**
7. Depends on the value of EFUSE_DIS_PAD_JTAG
   - 0 – WPU is enabled
   - 1 – pin floating

**Subtitle:** Some pins have glitches during power-up.

- See details in Table 2-2:

**Table Title:** Table 2-2. Power-Up Power-Up Glitches on Pins

| Pin       | Glitch                | Typical Time Period (µs) |
|-----------|-----------------------|--------------------------|
| GPIO1     | Low-level glitch      | 60                       |
| GPIO2     | Low-level glitch      | 60                       |
| GPIO3     | Low-level glitch      | 60                       |
| GPIO4     | Low-level glitch      | 60                       |
| GPIO5     | Low-level glitch      | 60                       |
| GPIO6     | Low-level glitch      | 60                       |
| GPIO7     | Low-level glitch      | 60                       |
| GPIO8     | Low-level glitch      | 60                       |
| GPIO9     | Low-level glitch      | 60                       |
| GPIO10    | Low-level glitch      | 60                       |
| GPIO11    | Low-level glitch      | 60                       |
| GPIO12    | Low-level glitch      | 60                       |
| GPIO13    | Low-level glitch      | 60                       |
| GPIO14    | Low-level glitch      | 60                       |
| XTAL_32K_P| Low-level glitch      | 60                       |
| XTAL_32K_N| Low-level glitch      | 60                       |
| GPIO17    | Low-level glitch      | Cont'd on next page     |

**Footer:**
Espressif Systems
ESP32-S3 Series Datasheet v2.1

[Submit Documentation Feedback](#)