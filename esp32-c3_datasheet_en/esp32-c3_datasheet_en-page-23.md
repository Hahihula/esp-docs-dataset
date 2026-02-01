**Title: Pins**

---

### Subtitle: 2.3.4 Peripheral Pin Assignment

**Body Text:**
Table **2-7 Peripheral Pin Assignment** highlights which pins can be assigned to each peripheral interface according to the following priorities:

1. **Priority 1**: Fixed pins connected directly to peripheral signals via IO MUX.
   - If a peripheral interface does not have priority 1 pins, such as UART1, it can be assigned to any GPIO pins from priority 2 to priority 4.

2. Any GPIO pins mapping to peripheral signals via GPIO Matrix, can be priority 2, 3, or 4:
   - **Priority 2**: GPIO pins can be freely used without restrictions.
   - **Priority 3**: GPIO pins should be used with caution, as they may conflict with the following important functions described in Section [**2.3.3 Restrictions for GPIOs**](#):
     * GPIO2, GPIO8, GPIO9: Strapping pins.
     * GPIO18, GPIO19: USB Serial/JTAG interface
     * GPIO4, GPIO5, GPIO6, GPIO7: JTAG interface.
     * GPIO20, GPIO21: UART0 interface.

3. **Priority 4**: The VDD_SPI pin is the power supply pin for flash by default and can only be reconfigured as a GPIO pin if the flash is powered by an external power supply:
   - **Priority 4**: GPIO pins already allocated or not recommended for use, as described in Section [**2.3.3 Restrictions for GPIOs**](#):
     * GPIO12, GPIO13, GPIO14, GPIO15, GPIO16, GPIO17: SPI0/1 interface connected to the in-package flash; or recommended for off-package flash.

If a peripheral interface does not have priority 2 to 4 pins (such as USB Serial/JTAG), it means it can be assigned only to priority 1 pins.

**Note:**
- For details about which peripheral signals are connected to IO MUX pins, please refer to Section [**2.3.1 IO MUX Functions**](#).
- For details about which peripheral signals can be assigned to GPIO pins, please refer to ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix > Section Peripheral Signal List.

---

**Footer:**
Espressif Systems  
ESP32-C3 Series Datasheet v2.2

[Submit Documentation Feedback](#)