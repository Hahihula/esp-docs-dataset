

```markdown
| 2 | GPIO input toggles from high-level to low-level | LP_GPIO_PINx_EDGE_WAKEUP_CLR is set |
|---|-----------------------------------------------|-------------------------------------|
| 3 | GPIO input toggles from high-level to low-level, or vice versa | LP_GPIO_PINx_EDGE_WAKEUP_CLR is set |
| 4 | GPIO input is low-level                        | GPIO input is high-level            |
| 5 | GPIO input is high-level                      | GPIO input is low-level             |

1 `x` ranges from 0 to 6.
2 If the field is configured to any other value, LP GPIO wakeup feature is disabled.

## 6.4.6 Programming Procedure

### 6.4.6.1 HP GPIO Matrix

To read GPIO pin X into HP peripheral signal Y, follow the steps below:

1. Configure `GPIO_FUNCy_IN_SEL_CFG_REG` corresponding to peripheral signal Y in HP GPIO matrix:
    * Set `GPIO_SIGy_IN_SEL` to enable peripheral signal input via HP GPIO matrix.
    * Set `GPIO_FUNCy_IN_SEL` to the desired GPIO pin, i.e., X here.

2. Optionally enable the GPIO Filter for pin input signals by setting `IO_MUX_GPIOx_FILTER_EN`.

3. Synchronize GPIO input signals. To do so, set `GPIO_PINx_REG` corresponding to GPIO pin X as follows:
    * Set `GPIO_PINx_SYNC1_BYPASS` to enable input signal synchronized on rising edge or on falling edge in the first-level synchronization, see Figure 6.4-1.
    * Set `GPIO_PINx_SYNC2_BYPASS` to enable input signal synchronized on rising edge or on falling edge in the second-level synchronization, see Figure 6.4-1.

4. Configure HP IO MUX register to enable pin input². For this end, set `IO_MUX_GPIOx_REG` corresponding to GPIO pin X as follows:
    * Set `IO_MUX_GPIOx_FUN_IE` to enable input³.
    * Set or clear `IO_MUX_GPIOx_FUN_WPU` and `IO_MUX_GPIOx_FUN_WPD` as desired to enable or disable pull-up and pull-down resistors.

**Note:**
1. One input pin can be connected to multiple peripheral input signals.
2. The input signal can be inverted by configuring `GPIO_FUNCy_IN_INV_SEL`.
3. It is possible to have an HP peripheral read a constantly low or constantly high input value without connecting this input to a pin. This can be done by selecting a special `GPIO_FUNCy_IN_SEL` input, instead of a GPIO number:
    * When `GPIO_FUNCy_IN_SEL` is set to 0x40, input signal is always 0.
    * When `GPIO_FUNCy_IN_SEL` is set to 0x60, input signal is always 1.

**Programming Example**

To connect UARTO RXD input signal (UORXD_in, signal index 6) to GPIO7, please follow the steps below.
```