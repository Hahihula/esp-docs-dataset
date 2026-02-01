**Title:**
2 Pins

**Subtitle:**
2.3.6 Peripheral Pin Assignment

**Body Text:**

Table **2-9 Peripheral Pin Assignment** highlights which pins can be assigned to each peripheral interface according to the following priorities:

- **Priority 1 (P1):** Fixed pins connected directly to peripheral signals via IO MUX or RTC IO MUX.
   - If a peripheral interface does not have priority 1 pins, such as UART2, it can be assigned to any GPIO pins from priority 2 to priority 4.

- Any GPIO pins mapping to peripheral signals via GPIO Matrix, can be priority 2, 3, or 4:
   - **Priority 2 (P2):** GPIO pins can be freely used without restrictions.
   - **Priority 3 (P3):** GPIO pins should be used with caution, as they may conflict with the following important functions described in Section [2.3.5 Restrictions for GPIOs and RTC_GPIOS](#):
      - *GPIO0, GPIO45, GPIO46:* Strapping pins.
      - *GPIO39, GPIO40, GPIO41, GPIO42:* ITAG interface.
      - *GPIO43, GPIO44:* UARTO interface.

- **Priority 4 (P4):** GPIO pins already allocated or not recommended for use, as described in Section [2.3.5 Restrictions for GPIOs and RTC_GPIOS](#):
   - *GPIO26, GPIO27, GPIO28, GPIO29, GPIO30, GPIO31, GPIO32:* SPI/O/1 interface connected to the in-package flash and PSRAM, or recommended for the off-package flash and PSRAM.

If a peripheral interface does not have priority 2 to 4 pins, such as USB Serial/JTAG, it means it can be assigned only to priority 1 pins.

**Note:**
- For details about which peripheral signals are connected to IO MUX or RTC IO MUX pins, please refer to Section [2.3.1 IO MUX Functions](#) or Section [2.3.3 RTC Functions](#).
- For details about which peripheral signals can be assigned to GPIO pins, please refer to ESP32-S2 Technical Reference Manual > Chapter 10 MUX and GPIO Matrix > Section Peripheral Signal List.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number:** 
23  

**Document Version:**
ESP32-S2 Series Datasheet v1.8