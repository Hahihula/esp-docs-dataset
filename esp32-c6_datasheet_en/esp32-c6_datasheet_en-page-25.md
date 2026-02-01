**Title:**
2 Pins

**Subtitle:**
2.3.5 Peripheral Pin Assignment

**Body Text:**

Table **2-10 QFN40 Peripheral Pin Assignment** and Table 2-11 QFN32 Peripheral Pin Assignment highlight which pins can be assigned to each peripheral interface according to the following priorities:

- **Priority 1 (P1):** Fixed pins connected directly to peripheral signals via IOMUX or RTC IO MUX. If a peripheral does not have priority 1 pins, such as UART1, it can be assigned to any GPIO pins from priority 2 to priority 4.

- Any GPIO pins mapping to peripheral signals via GPIO Matrix, can be priority 2, 3, or 4:
  - **Priority 2 (P2):** GPIO pins can be freely used without restrictions.
  - **Priority 3 (P3):** GPIO pins should be used with caution, as they may conflict with the following important functions described in Section [2.3.4 Restrictions for GPIOs and LP GPIOs](#):
    * GPIO4, GPIO5, GPIO8, GPIO9, GPIO15: Strapping pins.
    * GPIO12, GPIO13: USB Serial/JTAG interface.
    * GPIO4, GPIO5, GPIO6, GPIO7: JTAG interface.
    * GPIO16, GPIO17: UART0 interface.

- **GPIO27:** The VDD_SPI pin. The power supply pin for off-package flash by default, and can only be reconfigured as a GPIO pin if the flash is powered by an external power supply.

- **Priority 4 (P4):** GPIO pins already allocated or not recommended for use, as described in Section [2.3.4 Restrictions for GPIOs and LP GPIOs](#):
  * GPIO24, GPIO25, GPIO26, GPIO28, GPIO29, GPIO30: SPI/1 interface recommended for the off-package flash.

If a peripheral does not have priority to 2 or 4 pins, such as USB Serial/JTAG, it means it can be assigned only to priority 1 pins.

**Note:**
- For details about which peripheral signals are connected to IOMUX or LP IOMUX pins, please refer to Section [2.3.1 IOMUX Pin Functions](#) or Section [2-7 LP IOMUX Functions](#).
- For details about which peripheral signals can be assigned to GPIO pins, please refer to ESP32-C6 Technical Reference Manual > Chapter IO MUX and GPIO Matrix > Section Peripheral Signal List.

**Footer:**
Espressif Systems
Page 25 of ESP32-C6 Series Datasheet v1.4

[Submit Documentation Feedback](#)