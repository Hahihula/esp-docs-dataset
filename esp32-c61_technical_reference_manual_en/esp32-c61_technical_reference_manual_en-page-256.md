

```markdown
IE: input enable
OE: output enable
WPU: internal weak pull-up resistor enable
WPD: internal weak pull-down resistor enable
Bonding pad: a terminal point of the chip logic used to make a physical connection from the chip die to GPIO pin in the chip package
```

## 6.4 Peripheral Input via GPIO Matrix

### 6.4.1 Overview

To receive a peripheral input signal via HP GPIO matrix,

- Configure the matrix to source the peripheral input signal from one of the 22 GPIOs (0~13, 22~29), see Table 6.12-1.
- Configure the peripheral signal to receive input signal via HP GPIO matrix.
- Configure the GPIO pin to be controlled by HP IO MUX.

For detailed configuration, see Figure 6.3-1 and Section 6.4.6.

As shown in Figure 6.3-1, when GPIO matrix is used to input a signal from the pin, all external input signals are sourced from the GPIO pins and then filtered by the GPIO Filter, as shown in Step 2 in Section 6.4.6.

All signals filtered by the GPIO Filter hardware are synchronized by the GPIO SYNC hardware to IO MUX operating clock and then enter the GPIO matrix, see Section 6.4.2. Such signal filtering and synchronization features apply to all GPIO matrix signals but do not apply when using the IO MUX.

### 6.4.2 Signal Synchronization

Only HP GPIO matrix supports this signal synchronization function. Figure 6.4-1 shows the functionality of GPIO SYNC. In the figure, negative sync and positive sync mean GPIO input is synchronized on falling edge and on
```