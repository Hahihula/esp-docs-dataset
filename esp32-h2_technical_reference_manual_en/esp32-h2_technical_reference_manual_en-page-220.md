

```markdown
## 6.4.2 Signal Synchronization

Figure 6.4-1 shows the functionality of GPIO SYNC. In the figure, negative sync and positive sync mean GPIO input is synchronized on falling edge and on rising edge of IO MUX operating clock respectively.

The synchronization function is disabled by default by the synchronizer, i.e., `GPIO_PINx_SYNC1/2_BYPASS[1:0] = 0`. But when an asynchronous peripheral signal is connected to the pin, the signal should be synchronized by the two-level synchronizer (i.e., the first-level synchronizer and the second-level synchronizer as shown in Figure 6.4-1) to lower the probability of causing metastability. For more information, see Step 4 in the following section.

## 6.4.3 Functional Description

To read GPIO pin `X` into peripheral signal `Y`, follow the steps below:

1. Configure register `GPIO_FUNCy_IN_SEL_CFG_REG` corresponding to peripheral signal `Y` in GPIO matrix:
    - Set `GPIO_SIGy_IN_SEL` to enable peripheral signal input via GPIO matrix.
    - Set `GPIO_FUNCy_IN_SEL` to the desired GPIO pin, i.e., `X` here.

Note that some peripheral signals have no valid `GPIO_SIGy_IN_SEL` bit, namely, these peripherals can only receive input signals via GPIO matrix.

2. Optionally enable the GPIO Filter for pin input signals by setting `IO_MUX_GPIOx_FILTER_EN`. Only the signals with a valid width of more than two clock cycles can be sampled, see Figure 6.4-2.
```