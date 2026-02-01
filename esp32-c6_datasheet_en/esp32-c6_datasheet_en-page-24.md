**Title:**
2 Pins

**Subtitle:**
2.3.4 Restrictions for GPIOs and LP GPIOs

**Body Text:**

All IO pins of ESP32-C6 have GPIO and some have LP GPIO pin functions. However, the IO pins are multiplexed and can be configured for different purposes based on the requirements. Some IOs have restrictions for usage. It is essential to consider the multiplexed nature and the limitations when using these IO pins.

In tables of this chapter, some pin functions are highlighted in red or yellow which require extra caution when used as GPIO / GPIO:

- **IO Pins** – allocated for communication with flash and NOT recommended for other uses. For details, see Section 2.6 Pin Mapping Between Chip and Flash.
  
- IO Pins
  - have one of the following important functions:
    - Strapping pins — need to be at certain logic levels at startup. See Section 3 Boot Configurations.

**Note:**
Strapping pins are highlighted by Pin Name or configurations At Reset, instead of the pin functions.

- USB_D+/– – by default, connected to the USB Serial/JTAG Controller. To function as GPIOs, these pins need to be reconfigured.
  
- JTAG interface — often used for debugging. See Table 2-4 QFN40 IO MUX Pin Functions or Table 2-5 QFN32 IO MUX Pin Functions. To free these pins up, the pin functions USB_D+/- of the USB Serial/JTAG Controller can be used instead. See also Section 3.4 JTAG Signal Source Control.
  
- UARTO interface — often used for debugging. See Table 2-4 QFN40 IO MUX Pin Functions or Table 2-5 QFN32 IO MUX Pin Functions.

- VDD_SPI – the power supply pin for off-package flash by default, and can only be used as a GPIO pin if the flash is powered by an external power supply.

**Additional Information:**
For more information about assigning pins, please see Section 2.3.5 Peripheral Pin Assignment and ESP32-C6 Consolidated Pin Overview.

**Footer:**
Espressif Systems
ESP32-C6 Series Datasheet v1.4

**Link Texts in the Image:**
- Submit Documentation Feedback