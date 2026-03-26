

```markdown
Table 9.4-2. LP GPIO Wakeup Signal Trigger and Clear Conditions

| LP_GPIO_PINx_INT_TYPE¹,² | Wakeup is generated when                                                                 | Wakeup is cleared when                                                      |
|--------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| 1                        | the input GPIO toggles from low-level to high-level.                                     | `LP_GPIO_PINx_EDGE_WAKEUP_CLR` is set.                                      |
| 2                        | the input GPIO toggles from high-level to low-level.                                     | `LP_GPIO_PINx_EDGE_WAKEUP_CLR` is set.                                      |
| 3                        | the input GPIO toggles from high-level to low-level, or vice versa.                      | `LP_GPIO_PINx_EDGE_WAKEUP_CLR` is set.                                      |
| 4                        | the input GPIO is low-level.                                                              | the input GPIO is high-level.                                                |
| 5                        | the input GPIO is high-level.                                                             | the input GPIO is low-level.                                                 |

¹ x ranges from 0 to 15.
² If the register is configured to any other value, LP GPIO wakeup feature is disabled.

9.4.7 Programming Procedure

9.4.7.1 HP GPIO Matrix

To read GPIO pin X¹ into HP peripheral signal Y, follow the steps below:

1. Configure `GPIO_FUNCy_IN_SEL_CFG_REG` corresponding to HP peripheral signal Y in HP GPIO matrix:
   - Set `GPIO_SIGy_IN_SEL` to enable peripheral signal input via HP GPIO matrix.
   - Set `GPIO_FUNCy_IN_SEL` to the desired GPIO pin, i.e., X here.

Note that some peripheral signals have no valid `GPIO_SIGy_IN_SEL` bit, namely, these peripherals can only receive input signals via HP GPIO matrix.

2. Optionally enable the GPIO Filter for pin input signals by setting `IO_MUX_GPIOn_FILTER_EN`.

3. Enable Glitch Filter feature as follows:
   - Configure `GPIO_EXT_FILTER_CHn_INPUT_IO_NUM` to m. n (0 ~ 7) represents the channel number. m (0 ~ 54) represents the GPIO pin number.
   - Configure `GPIO_EXT_FILTER_CHn_WINDOW_WIDTH` to VALUE1 and `GPIO_EXT_FILTER_CHn_WINDOW_THRES` to VALUE2. During VALUE1 + 1 cycles, if there are VALUE2 + 1 input signals that do not match the current output signal value, the Glitch Filter hardware inverts the output signal. `GPIO_EXT_FILTER_CHn_WINDOW_WIDTH` and `GPIO_EXT_FILTER_CHin_WINDOW_THRES` can be configured to the same value VALUE3, then only signals with a width greater than VALUE3 + 1 clock cycles will be sampled.
   - Set `GPIO_EXT_FILTER_CHn_EN` to enable channel n.

An example is shown in Figure 9.4-3, where `GPIO_EXT_FILTER_CHx_WINDOW_WIDTH` is configured to 3 and `GPIO_EXT_FILTER_CHx_WINDOW_THRES` to 2. The output signal value (signal_out) keeps as “0” in the four clock cycles before. The input signal value (signal_in) has been “1” for three clock cycles in the same period, then the output signal is inverted to “1” after T1.
```