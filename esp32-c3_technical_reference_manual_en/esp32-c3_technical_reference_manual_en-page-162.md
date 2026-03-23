

```markdown
## 5.4.2 Signal Synchronization

When signals are directed from pins using GPIO matrix, the signals will be synchronized to the APB bus clock by GPIO SYNC hardware, then go to GPIO matrix. This synchronization applies to all GPIO matrix signals but does not apply when using the IO MUX, see Figure 5.3-2.

![GPIO input sync](image_path)  
Figure 5.4-1. GPIO Input Synchronized on APB Clock Rising Edge or on Falling Edge

Figure 5.4-1 shows the functionality of GPIO SYNC. In the figure, negative sync and positive sync mean GPIO input is synchronized on APB clock falling edge and on APB clock rising edge, respectively.

## 5.4.3 Functional Description

To read GPIO pin X into peripheral signal Y, follow the steps below:

1. Configure register `GPIO_FUNCy_IN_SEL_CFG_REG` corresponding to peripheral signal Y in GPIO matrix:
    - Set `GPIO_SIGy_IN_SEL` to enable peripheral signal input via GPIO matrix.
    - Set `GPIO_FUNCy_IN_SEL` to the desired GPIO pin, i.e. X here.

Note that some peripheral signals have no valid `GPIO_SIGy_IN_SEL` bit, namely, these peripherals can only receive input signals via GPIO matrix.

2. Optionally enable the filter for pin input signals by setting the register `IO_MUX_GPIOx_FILTER_EN`. Only the signals with a valid width of more than two clock cycles can be sampled, see Figure 5.4-2.

![Filter Timing](image_path)  
Figure 5.4-2. Filter Timing of GPIO Input Signals

3. Synchronize GPIO input. To do so, please set `GPIO_PINx_REG` corresponding to GPIO pin X as follows:
```