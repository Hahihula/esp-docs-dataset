**Title: Pins**

---

### Control

1. **In column Pin Providing Power, regarding pins powered by VDD_LP / VDD_BAT:**  
   - Pin Providing Power (either VDD_LP or VDD_BAT) can be configured via a register.

2. **Default drive strength for IO pins is 20 mA except for GPIO24 and GPIO25 which have default drive strength of 40 mA.**

3. **Column Pin Settings** shows predefined settings at reset and after reset with the following abbreviations:
   - IE – input enabled
   - WPU – internal weak pull-up resistor enabled
   - USB PU – USB pull-up resistor enabled

   By default, the USB function is enabled for USB pins (i.e., GPIO24/26 and GPIO25/27), and the pin pull-up is decided by the USB pull-up. The USB pull-up control is controlled by USB_SERIAL_JTAG_DP/DM_PULLUP and the pull-up resistor value is controlled by USB_SERIAL_JTAG_PULLUP_VALUE.

   When the USB function is disabled, USB pins are used as regular GPIOs and the pins' internal weak pull-up and pull-down resistors are disabled by default (configurable by IOca_MUX_GIOx FUNCTION_WPU/WPD).

4. **Depends on the value of EFUSE_DIS_PAD_JTAG**
   - 0 (default), input enabled, pull-up resistor enabled (IE = 1, WPU = 1)
   - Input disabled in high impedance state (IE = 0)

---

**Footer:**

- Page number: "17"
- Company name: Espressif Systems
- Document title: ESP32-P4 Series Datasheet v0.6
- Link text: Submit Documentation Feedback