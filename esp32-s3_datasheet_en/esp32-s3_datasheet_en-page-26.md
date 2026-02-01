**Title:**
2 Pins

**Subtitle:**
2.3.5 Peripheral Pin Assignment

**Table Reference and Description:**
- **Table Title:** Table 2–9 Peripheral Pin Assignment highlights which pins can be assigned to each peripheral interface according to the following priorities:

**Body Text with List Structure:**

1. **Priority (P1):**
   - Fixed pins connected directly to peripheral signals via IO MUX or RTC IO MUX.
   - If a peripheral interface does not have priority 1 pins, such as UART2, it can be assigned to any GPIO pins from priority 2 to priority 4.

2. **Any GPIO pins mapping to peripheral signals via GPIO Matrix:**
   - Can be prioritized based on the following:
     - Priority (P2): GPIO pins are freely used without restrictions.
     - Priority (P3): GPIO pins should use with caution, as they may conflict with important functions described in Section 2.3.4 Restrictions for GPIOs and RTC_GPIOs:

       * GPIO0, GPIO3, GPIO45, GPIO46: Strapping pins.

       * GPIO19, GPIO20: USB Serial/JTAG interface.
       
       * GPIO39, GPIO40, GPIO41, GPIO42: JTAG interface.
       
       * GPIO43, GPIO44: UART0 interface.
       
       * GPIO33, GPIO34, GPIO35, GPIO36, GPIO37: The higher 4 bits data line interface and DQS interface for the SPI/1 interface in 8-line SPI mode. Can be GPIO pins if chip is not connected to flash or PSRAM in 8-line SPI mode.

     - Priority (P4): GPIO pins already allocated or are recommended against use, as described in Section 2.3.4 Restrictions for GPIOs and RTC_GPIOs:

       * GPIO26, GPIO27, GPIO28, GPIO29, GPIO30, GPIO31, GPIO32: SPI/1 interface connected to the in-package flash and PSRAM.

**Additional Information (Note):**
- For details about which peripheral signals are assigned directly via IO MUX or RTC IO MUX pins:
  - Refer to Section 2.3.1 IO MUX Functions.
  
- For details on which peripheral signals can be assigned to GPIO pins, refer to ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix > Section Peripheral Signal List.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** 26
**Document Version:** ESP32-S3 Series Datasheet v2.1