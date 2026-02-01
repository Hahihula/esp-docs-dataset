**Title:**
2 Pins

**Subtitle:**
2.3.4 Restrictions for GPIOs and LP GPIOs

**Body Text:**

All IO pins of ESP32-C61 have GPIO and some have RTC_GPIO pin functions. However, the IO pins are multiplexed and can be configured for different purposes based on the requirements. Some IOs have restrictions for usage. It is essential to consider the multiplexed nature and the limitations when using these IO pins.

In tables of this chapter, some pin functions are highlighted. The non-highlighted GPIO or RTC_GPIO pins are recommended for use first. If more pins are needed, the highlighted GPIOs or RTC_GPIOS should be chosen carefully to avoid conflicts with important pin functions.

The highlighted IO pins have the following important pin functions:

- **GPIO** – allocated for communication with in-package flash/PSRAM and NOT recommended for other uses. For details, see Section 2.6 Pin Mapping Between Chip and Flash/PSRAM.
  
- **GPIO** – have one of the following important functions:
  - Strapping pins – need to be at certain logic levels at startup. See Section 3 Boot Configurations.
  - USB_D+/- by default, connected to the USB Serial/JTAG Controller. To function as GPIOs, these pins need to be reconfigured.

- JTAG interface – often used for debugging. See Table 2-2 IO MUX Functions. To free these pins up, the pin functions USB_D+/- of the USB Serial/JTAG Controller can be used instead. See also Section 3.4 JTAG Signal Source Control.
  
- UART interface – often used for debugging. See Table 2-2 IO MUX Functions.

**Footer:**
See also Appendix A – ESP32-C61 Consolidated Pin Overview

**Page Information:**
Espressif Systems
ESP32-C61 Series Datasheet v0.5