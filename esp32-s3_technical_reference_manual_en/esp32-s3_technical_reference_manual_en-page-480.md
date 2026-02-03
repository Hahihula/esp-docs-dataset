**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Section Title:
6.7.2 Low Power Capabilities

**Body Text:**
The pins with RTC functions are controlled by `RTC_IO_TOUCH/RTC_PADn_MUX_SEL` bit in register `RTC_IO TOUCH/RTC_PADn REG`. By default all bits in these registers are set to 0, routing all input/output signals via IO MUX.

If `RTC_IO_TOUCH/RTC_PADn_MUX_SEL` is set to 1, then input/output signals to and from that pin is routed to the RTC subsystem. In this mode, `RTC_IO TOUCH/RTC_PADn REG` is used to control RTC low power pins.
Note that `RTC_IO TOUCH/RTC_PADn REG` applies the RTC GPIO pin numbering, not the GPIO pin numbering.

See Table 6.13-1 for RTC functions of RTC IO MUX pins.

---

### Section Title:
6.7.3 Analog Functions

**Body Text:**
When the pin is used for analog purpose, make sure this pin is left floating by configuring the register `RTC_IO TOUCH /RTC_PADn REG`. By such way, external analog signal is connected to internal analog signal via GPIO pin. The configuration is as follows:

- Set `RTC_IO TOUCH/RTC_PADn MUX_SEL`, to select RTC IO MUX to route input and output signals.
- Clear `RTC_IO TOUCH/RTC_PADn FUN IE`, `RTC_IO TOUCH/RTC_PADn FUN RDE`, to set this pin floating.
- Configure `RTC_IO TOUCH/RTC_PADn FUN SEL` to 0, to enable analog function 0.

Write 1 to `RTC_GPIO_ENABLE W1TC`, to clear output enable.

See Table 6.13-2 for analog functions of RTC IO MUX pins.

---

### Section Title:
6.8 Pin Functions in Light-sleep

**Body Text:**
Pins may provide different functions when ESP32-S3 is in Light-sleep mode. If `IO MUX_SLP SEL` in register `IO MUX n REG` for a GPIO pin is set to 1, a different set of bits will be used to control the pin when the chip is in Light-sleep mode.

---

**Table Title:**
Table 6.8-1. Bits Used to Control IO Mux Functions in Light-sleep Mode

| IO MUX Functions | Normal Execution | Light-sleep Mode |
|------------------|-------------------|------------------|
| OR `IO MUX SLP SEL` = 0 | AND `IO MUX SLP SEL` = 1 |

**Table Content:**
- Output Drive Strength
  - `IO MUX FUN DRV`
  - `IO MUX MCU_DRV`

- Pull-up Resistor
  - `IO MUX FUN WPU`
  - `IO MUX MCU WPU`

- Pull-down Resistor
  - `IO MUX FUN WPD`
  - `IO MUX MCU WPD`

- Output Enable
  - `OEN SEL` from GPIO matrix *
  - `IO MUX MCU OE`

**Note:**
If `IO MUX SLP SEL` is set to 0, pin functions remain the same in both normal execution and Light-sleep mode. Please refer to Section 6.5.2 for how to enable output in normal execution.

---

**Footer Information:**
Espressif Systems  
480 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback