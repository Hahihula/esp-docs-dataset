**Title:**
2 Pins

**Subtitle:**
2.3.3 Restrictions for GPIOs

**Body Text:**

All IO pins of ESP32-C3 have GPIO pin functions. However, the IO pins are multiplexed and can be configured for different purposes based on the requirements. Some IOs have restrictions for usage. It is essential to consider the multiplexed nature and the limitations when using these IO pins.

In tables of this chapter, the following pin functions are highlighted in red or yellow. These functions indicate pins that require extra caution when used as GPIO / GPIO :

- **IO Pins** – allocated for communication with in-package flash and NOT recommended for other uses.
  - For details, see Section [2.6 Pin Mapping Between Chip and Flash](#).

- IO Pins
  - have one of the following important functions:
    - Strapping pins — need to be at certain logic levels at startup. See Section [3 Boot Configurations](#).
      - Note: Strapping pins are highlighted by Pin Name or configurations At Reset, instead of the pin functions.
    - USB_D+//- – by default, connected to the USB Serial/JTAG Controller. To function as GPIOs, these pins need to be reconfigured.
    - JTAG interface — often used for debugging. See Table [2-3 Peripheral Signals Routed via IO MUX](#). To free these pins up, the pin functions USB_D+/- of the ESP32-C3 Technical Reference Manual USB Serial/JTAG Controller can be used instead.
    - UART0 interface — often used for debugging. See Table [2-3 Peripheral Signals Routed via IO MUX](#).
    - VDD_SPI – the power supply pin for flash by default, and can only be used as a GPIO pin if the flash is powered by an external power supply.

For more information about assigning pins, please see Section [2.3.4 Peripheral Pin Assignment](#) and ESP32-C3 Consolidated Pin Overview.

**Footer:**
Espressif Systems
ESP32-C3 Series Datasheet v2.2

**Link Texts in the Body:**

- 2.6 Pin Mapping Between Chip and Flash.
- Section [3 Boot Configurations](#).
- Table 2-3 Peripheral Signals Routed via IO MUX (repeated twice for emphasis, as it appears to be a reference or table of contents link).

**Note:** The text includes references marked with "[ ]" which are likely placeholders indicating sections in the document that need further elaboration.