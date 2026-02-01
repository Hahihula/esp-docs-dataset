**Title:**
2 Pins

**Subtitle:**
2.3.3 Restrictions for GPIOs

**Body Text:**

All IO pins of ESP32-H2 have GPIO pin functions. However, the IO pins are multiplexed and can be configured for different purposes based on the requirements. Some IOs have restrictions for usage. It is essential to consider the multiplexed nature and the limitations when using these IO pins.

In tables of this chapter, some pin functions are highlighted. The non-highlighted GPIO pins are recommended for use first. If more pins are needed, the highlighted GPIOs should be chosen carefully to avoid conflicts with important pin functions.

The highlighted 10 pins have the following important pin functions:

- **Strapping pins** – need to be at certain logic levels at startup. See Section 3 Boot Configurations.
- USB_D+/- by default, connected to the USB Serial/JTAG Controller. To function as GPIOs, these pins need to be reconfigured.

- JTAG interface - often used for debugging. See Table 2-2 Peripheral Signals Routed via IO MUX. To free these pins up, the pin functions USB_D+/- of the USB Serial/JTAG Controller can be used instead. See also Section 3.3 JTAG Signal Source Control.
  
- UART interface – often used for debugging. See Table 2-2 Peripheral Signals Routed via IO MUX.

**Footer:**
See also Appendix A - ESP32-H2 Consolidated Pin Overview

**Page Information:**
Espressif Systems
ESP32-H2 Series Datasheet v1.2
Submit Documentation Feedback