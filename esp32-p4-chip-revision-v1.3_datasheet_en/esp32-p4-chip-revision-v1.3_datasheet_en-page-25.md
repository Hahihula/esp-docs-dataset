**Title:**
2 Pins

**Subtitle:**
2.3.4 Restrictions for GPIOs and LP GPIOs

**Body Text:**
All IO pins of ESP32-P4 have GPIO pin functions, and some have LP GPIO pin functions. However, the IO pins are multiplexed and can be configured for different purposes based on the requirements. Some IOs have restrictions for usage. It is essential to consider the multiplexed nature and the limitations when using these IO pins.

In tables of this chapter, some pin functions are highlighted[^1]. The non-highlighted GPIO or LP_GPIO pins are recommended for use first. If more pins are needed, the highlighted GPIOs or LP_GPIOS should be chosen carefully to avoid conflicts with important pin functions.

**Highlighted Section:**
The highlighted IO pins have one of the following important functions:

- **Strapping pins** – need to be at certain logic levels at startup. See Section 3 Boot Configurations.
  
- USB1P1_NO/PO – by default, connected to the USB Serial/JTAG Controller. To function as GPIOs, these pins need to be reconfigured.

- JTAG interface – often used for debugging. See Table 2-2 IO MUX Functions[^2]. To free these pins up, the pin functions USB1P1_N/P of the USB Serial/JTAG Controller can be used instead. See also Section 3.4 JTAG Signal Source Control.

- UART interface – often used for debugging. See Table 2-2 IO MUX Functions[^2].

**References:**
See also Appendix A – ESP32-P4 Consolidated Pin Overview.

**Footer:**
Espressif Systems
ESP32-P4 Series Datasheet v0.6

[1] The non-highlighted GPIO or LP_GPIO pins are recommended for use first.
[2] To free these pins up, the pin functions USB1P1_N/P of the USB Serial/JTAG Controller can be used instead.

**Note:**
The image contains a watermark "PRELIMINARY" diagonally across it.