**Title: Pins**

---

### Table

| Pin No. | Pin Name | Pin Type | Pin Providing Power (2-4) | Pin Settings At Reset | After Reset |
|---------|----------|----------|----------------------------|-----------------------|-------------|
| 21      | SPICSO   | IO       | VDD_SPI / VDD3P3_CPU        | WPU                   | IE, WPU     |
| 22      | SPICLK   | IO       | VDD_SPI / VDD3P3_CPU        | WPU                   | IE, WPU     |
| 23      | SPID     | IO       | VDD_SPI / VDD3P3_CPU        | WPU                   | IE, WPU     |
| 24      | SPIQ     | IO       | VDD_SPI / VDD3P3_CPU        | WPU                   | IE, WPU     |
| 25      | GPIO18   | IO       | VDD3P3_CPU                  | WPU                   | IO MUX      |
| 26      | GPIO19   | IO       | VDD3P3_CPU                  | USB_PU               | IO MUX      |
| 27      | UORXD    | IO       | VDD3P3_CPU                  | IE, WPU              | IO MUX      |
| 28      | UOTXD    | IO       | VDD3P3_CPU                  | WPU                  | IO MUX      |
| 29      | XTAL_N   | Analog   |                             |                       |             |
| 30      | XTAL_P   | Analog   |                             |                       |             |
| 31      | VDDA     | Power    |                             |                       |             |
| 32      | VDDA     | Power    |                             |                       |             |
| 33      | GND      | Ground   |                             |                       |             |

---

### Notes

- **Bold** marks the pin function set in which a pin has its default function in the default boot mode. See Section [Chip Boot Mode Control](#).
  
- In column "Pin Providing Power", regarding pins powered by VDD_SPI:
  - Power actually comes from the internal power rail supplying power to VDDSPI. For details, see Section [Power Scheme](#).

- In column "Pin Providing Power" for VDD3P3_CPU / VDD_SPI:
  - Pin Providing Power (either VDD3P3_CPU or VDD_SPI) can be configured via a register; refer to the ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

- The default drive strength for each pin is as follows:

  | GPIO2, GPIO3, MTMS, and MTDI: 10 mA |
  | GPIO18, GPIO19: 40 mA               |
  | All other pins: 20 mA                |

### Column Pin Settings

Column "Pin Settings" shows predefined settings at reset after reset with the following abbreviations:

- **IE**: input enabled
- WPU: internal weak pull-up resistor enabled
- WPD: internal weak pull-down resistor enabled
- USB_PU: USB pull-up resistor enabled
  
  - By default, the USB function is enabled for USB pins (i.e., GPIO18 and GPIO19), and the pin pull-up or down resistors are controlled by the USB pull-up resistor. The USB pull-up resistor is controlled via USB_SERIAL_JTAG_DP/DM_PULUP and the pull-up value can be configured in Chapter [USB Serial/JTAG Controller](#).

- When the USB function is disabled, USB pins use regular GPIOs as well.

### Output

- **Output enabled**

### By default VDD_SPI power supply pin for:

- In-package
- Off-package flash
  
  - It may also reconfigure as a GPIO pin if connected to an off-package flash and powered by external supplies. Refer to the ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

### For ESP32-C3F4AZ

- Pins within the frame (namely pin 19 ~ pin 24) are not bonded, labeled as "not connected".

---

**Footer**

Espressif Systems  
[Submit Documentation Feedback](#)

ESP32-C3 Series Datasheet v2.2