

# 9.4 Peripheral Input via GPIO Matrix

## 9.4.1 Overview

To receive a peripheral input signal via HP GPIO matrix,

* configure the matrix to source the peripheral input signal from one of the 55 GPIOs (0 ~ 54), see Table 9.12-1.
* configure the peripheral signal to receive input signal via HP GPIO matrix.
* configure the GPIO pin to be controlled by HP IO MUX.

For detailed configuration, see Figure 9.3-1 and Section 9.4.7.

To receive a peripheral input signal via LP GPIO matrix,

* configure the matrix to source the peripheral input signal from one of the 16 GPIOs (0 ~ 15), see Table 9.13-1.
* configure the peripheral signal to receive input signal via LP GPIO matrix.
* configure the LP GPIO pin to be controlled by LP IO MUX.

For detailed configuration, see Figure 9.3-1 and Section 9.4.7.

As shown in Figure 9.3-1, when GPIO matrix is used to input a signal from the pin, all external input signals are sourced from the GPIO pins and then filtered by the GPIO Filter, as shown in Step 2 in Section 9.4.7.

The Glitch Filter is only available in HP GPIO matrix. The Glitch Filter hardware can filter eight of the output signals from the GPIO Filter, and the other unselected signals go directly to the GPIO SYNC hardware, as shown in Step 3 in Section 9.4.7.

All signals filtered by the GPIO Filter hardware or the Glitch Filter hardware are synchronized by the GPIO SYNC hardware to IO MUX operating clock and then enter the GPIO matrix, see Section 9.4.2. Such signal filtering and synchronization features apply to all GPIO matrix signals but do not apply when using the IO MUX.

## 9.4.2 Signal Synchronization

Only HP GPIO matrix supports this signal synchronization function. Figure 9.4-1 shows the functionality of GPIO SYNC. In the figure, negative sync and positive sync mean GPIO input is synchronized on falling edge and on rising edge of HP IO MUX operating clock respectively.