

```markdown
Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX)
GoBack

7.4.1 Overview

To receive a peripheral input signal via GPIO matrix, the matrix is configured to source the peripheral input signal from one of the 31 GPIOs (0 ~ 30), see Table 7.1-1. Meanwhile, the register corresponding to the peripheral signal should be set to receive input signal via GPIO matrix.

As shown in Figure 7.3-1, when GPIO matrix is used to input a signal from the pin, all external input signals are sourced from the GPIO pins and then filtered by the GPIO Filter, as shown in Step 2 in Section 7.4.3.

The Glitch Filter hardware can filter eight of the output signals from the GPIO Filter, and the other unselected signals go directly to the GPIO SYNC hardware, as shown in Step 3 in Section 7.4.3.

All signals filtered by the GPIO Filter hardware or the Glitch Filter hardware are synchronized by the GPIO SYNC hardware to IO MUX operating clock and then enter the GPIO matrix, see Section 7.4.2. Such signal filtering and synchronization features apply to all GPIO matrix signals but do not apply when using the IO MUX.

7.4.2 Signal Synchronization

Figure 7.4-1 shows the functionality of GPIO SYNC. In the figure, negative sync and positive sync mean GPIO input is synchronized on falling edge and on rising edge of IO MUX operating clock respectively.

The synchronization function is disabled by default by the synchronizer, i.e., `GPIO_PINx_SYNC1/2_BYPASS[1:0] = 0`. But when an asynchronous peripheral signal is connected to the pin, the signal should be synchronized by the two-level synchronizer (i.e., the first-level synchronizer and the second-level synchronizer as shown in Figure 7.4-1) to lower the probability of causing metastability. For more information, see Step 4 in the following section.

7.4.3 Functional Description

To read GPIO pin X into peripheral signal Y, follow the steps below:
```