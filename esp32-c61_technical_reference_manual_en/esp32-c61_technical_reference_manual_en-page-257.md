

```markdown
rising edge of HP IO MUX operating clock respectively.

Figure 6.4-1. GPIO Input Synchronized on Rising Edge or on Falling Edge of HP IO MUX Operating Clock

The synchronization function is disabled by default by the synchronizer. But when an asynchronous peripheral signal is connected to the pin, the signal should be synchronized by the two-level synchronizer (i.e., the first-level synchronizer and the second-level synchronizer as shown in Figure 6.4-1) to lower the probability of causing metastability.

6.4.3 GPIO Filter

Only HP GPIO matrix supports this GPIO Filter function. When this function is enabled, only signals with a valid width of more than two clock cycles can be sampled, as illustrated in Figure 6.4-2.

Figure 6.4-2. GPIO Filter Timing of GPIO Input Signals

6.4.4 Simple GPIO Input

Both the HP GPIO matrix and LP GPIO matrix support the Simple GPIO Input function. Enabling this function allows the direct reading of the input value of a GPIO pin at any time, without the need to route the GPIO input to any peripherals.

For HP GPIO matrix, to implement simple GPIO input, follow the steps below:

• Set IO_MUX_GPIOx_MCU_IE in IO_MUX_GPIOx_REG, to enable pin input.
```