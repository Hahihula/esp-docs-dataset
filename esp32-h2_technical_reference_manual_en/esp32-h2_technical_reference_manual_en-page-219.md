

```markdown
Figure 6.3-2. Internal Structure of a Pad

*   IE: input enable
*   OE: output enable
*   WPU: internal weak pull-up resistor
*   WPD: internal weak pull-down resistor
*   Bonding pad: a terminal point of the chip logic used to make a physical connection from the chip die to GPIO pin in the chip package

## 6.4 Peripheral Input via GPIO Matrix

### 6.4.1 Overview

To receive a peripheral input signal via GPIO matrix, the matrix is configured to source the peripheral input signal from one of the 19 GPIOs (0 = 5, 8 ~ 14, 22 ~ 27), see Table 6.12-1. Meanwhile, the register corresponding to the peripheral signal should be set to receive input signal via GPIO matrix.

As shown in Figure 6.3-1, when GPIO matrix is used to input a signal from the pin, all external input signals are sourced from the GPIO pins and then filtered by the GPIO Filter, as shown in Step 2 in Section 6.4.3.

The Glitch Filter hardware can filter eight of the output signals from the GPIO Filter, and the other unselected signals go directly to the GPIO SYNC hardware, as shown in Step 3 in Section 6.4.3.

All signals filtered by the GPIO Filter hardware or the Glitch Filter hardware are synchronized by the GPIO SYNC hardware to IO MUX operating clock and then enter the GPIO matrix, see Section 6.4.2. Such signal filtering and synchronization features apply to all GPIO signals but do not apply when using the IO MUX.
```