**Title:**
2 Pins

**Subtitle:**
2.3.4 Restrictions for GPIOs and LP GPIOs

**Body Text:**

All IO pins of the ESP32-C5 have GPIO and some have LP GPIO pin functions. However, the IO pins are multiplexed and can be configured for different purposes based on the requirements. Some IOs have restrictions for usage. It is essential to consider the multiplexed nature and the limitations when using these IO pins.

In tables of this chapter, some pin functions are highlighted. The non-highlighted GPIO or LP GPIO pins are recommended for use first. If more pins are needed, the highlighted GPIOs or LP GPIOs should be chosen carefully to avoid conflicts with important pin functions.

The highlighted IO pins have the following important pin functions:

- **GPIO** – allocated for communication with flash/PSRAM and NOT recommended for other uses. For details, see Section 2.6 Pin Mapping Between Chip and Flash/PSRAM.
  
- **GPIO** – have one of the following important functions:
  - Strapping pins – need to be at certain logic levels at startup. See Section 3 Boot Configurations.

Note: 
Strapping pins are highlighted by pin name, instead of pin functions.

- USB_D+/- – by default, connected to the USB Serial/JTAG controller. To function as GPIOs, these pins need to be reconfigured.
  
- JTAG interface – often used for debugging. See Table 2-2 Peripheral Signals Routed via IO MUX. To free these pins up, the pin functions USB_D+/- of the USB Serial/JTAG controller can be used instead. See also Section 3.4 JTAG Signal Source Control.

- UART interface – often used for debugging. See Table 2-2 Peripheral Signals Routed via IO MUX.
  
- SDIO interface – multiplexed with the pins for the USB Serial/JTAG controller. The SDIO Slave controller can be used together with the USB Serial/JTAG controller in single SPI mode, but not in quad SPI mode.

**Footer:**
See also Appendix A - ESP32-C5 Consolidated Pin Overview.
Espressif Systems
ESP32-C5 Series Datasheet v1.0

**Link Texts:**
Submit Documentation Feedback