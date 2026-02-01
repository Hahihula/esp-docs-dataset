**Title: Pins**

---

### Subtitle: 2.3.5 Restrictions for GPIOs and RTC_GPIOs

All IO pins of ESP32-S2 have GPIO and some have RTC_GPIO pin functions. However, the IO pins are multiplexed and can be configured for different purposes based on the requirements. Some IOs have restrictions for usage. It is essential to consider the multiplexed nature and the limitations when using these IO pins.

In tables of this chapter, some pin functions are in red or yellow. These functions indicate pins that require extra caution when used as GPIO / GPIO:

- **IO Pins** – allocated for communication with in-package flash/PSRAM and NOT recommended for other uses. For details, see Section 2.6 Pin Mapping Between Chip and Flash/PSRAM.
  
- **IQ Pins** – have one of the following important functions:
  - Strapping pins – need to be at certain logic levels at startup. See Section 3 Boot Configurations.

Note: 
Strapping pins are highlighted by Pin Name or configurations At Reset, instead of the pin functions:

- USB_D+/- -- by default, connected to the USB OTG. To function as GPIOs, these pins need to be reconfigured.
  
- JTAG interface – often used for debugging. See Table 2-2 Peripheral Signals Routed via IO MUX.

- UART0 interface – often used for debugging. See Table 2-2 Peripheral Signals Routed via IO MUX.

- **8-line SPI interface** -- no restrictions, unless the chip is connected to flash/PSRAM using 8-line SPI mode.

For more information about assigning pins, please see Section [2.3.6 Peripheral Pin Assignment](#) and ESP32-S2 Consolidated Pin Overview.

---

*Footer:*
Espressif Systems
ESP32-S2 Series Datasheet v1.8

Submit Documentation Feedback