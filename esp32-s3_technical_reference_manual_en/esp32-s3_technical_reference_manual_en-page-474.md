**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Figure Caption:**
Figure 6.3-2. Internal Structure of a Pad

**Diagram Labels in Image:**
- Routing to a peripheral
- OE
- Buf
- Routing from a peripheral
- WPU
- Bonding pad
- VDD3P3
- GND
- WPD

**Note Section (in the image):**
- IE: input enable
- OE: output enable
- WPU: internal weak pull-up
- WPD: internal weak pull-down
- Bonding pad: a terminal point of the chip logic used to make a physical connection from the chip die to GPIO pin in the chip package.

**Subtitles and Sections with Content:**
6.4 Peripheral Input via GPIO Matrix

   6.4.1 Overview
   To receive a peripheral input signal via GPIO matrix, the matrix is configured to source the peripheral input signal from one of the 45 GPIOs (0 ~ 21, 26 ~ 48), see Table 6.11-1. Meanwhile, register corresponding to the peripheral signal should be set to receive input signal via GPIO matrix.

   6.4.2 Signal Synchronization
   When signals are directed from pins using the GPIO matrix, the signals will be synchronized to the APB bus clock by the GPIO SYNC hardware, then go to GPIO matrix. This synchronization applies to all GPIO matrix signals but does not apply when using the IO MUX, see Figure 6.3-1.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)