

```markdown
⑥ There are peripheral inputs only through HP IO MUX.
⑦ There are peripheral outputs only through HP IO MUX.

Figure 8.3-2 shows the internal structure of a pad, which is an electrical interface between the chip logic and the GPIO pin. The structure is applicable to all GPIO pins and can be controlled using IE, OE, WPU, and WPD signals. For the configuration of these signals, see IO_MUX_GPIOx_REG or LP_IO_MUX_GPIOx_REG.

Routing to a peripheral

IE
VDD
WPU
OE
Buf
GND
WPD
Bonding pad

Figure 8.3-2. Internal Structure of a Pad

• IE: input enable
• OE: output enable
• WPU: internal weak pull-up resistor
• WPD: internal weak pull-down resistor
• Bonding pad: a terminal point of the chip logic used to make a physical connection from the chip die to GPIO pin in the chip package

8.4 Peripheral Input via GPIO Matrix

8.4.1 Overview

To receive a peripheral input signal via HP GPIO matrix,

• Configure the matrix to source the peripheral input signal from one of the 21 GPIOs (0~14, 23~28), see Table 8.12-1.
• Configure the peripheral signal to receive input signal via HP GPIO matrix.
• Configure the GPIO pin to be controlled by HP IO MUX.

For detailed configuration, see Figure 8.3-1 and Section 8.4.7.
```