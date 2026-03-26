

```markdown
## 9.4.5 Simple GPIO Input

Both the HP GPIO matrix and LP GPIO matrix support the Simple GPIO Input function. Enabling this function allows the direct reading of the input value of a GPIO pin at any time, without the need to route the GPIO input to any peripherals.

For HP GPIO matrix, to implement simple GPIO input, follow the steps below:

*   Set `IO_MUX_GPIOx_MCU_IE` in `IO_MUX_GPIOx_REG`, to enable pin input.
*   Read the GPIO input from `GPIO_IN_REG[x]`.

For LP GPIO matrix, to implement simple GPIO input, follow the steps below:

*   Set `LP_IOMUX_PADx_FUNC_IE` in `LP_IO_MUX_PADx_REG`, to enable pin input.
*   Read the GPIO input from `LP_GPIO_IN_REG[x]`.

## 9.4.6 GPIO Wakeup

### 9.4.6.1 HP GPIO Wakeup

The HP GPIO wakeup feature is designed to awaken the system from Light-sleep when the HP system is in clock gating mode. HP GPIO wakeup is not available when the HP system is powered down.

GPIO0 ~ GPIO54 can be used to generate HP GPIO wakeup by enabling `GPIO_PINx_WAKEUP_ENABLE` (x: 0 ~ 54).

HP GPIO wakeup supports both high-voltage sensitive and low-voltage sensitive wakeups, with specific conditions based on the GPIO configuration.

**Table 9.4-1. HP GPIO Wakeup Signal Trigger and Clear Conditions**

| `GPIO_PINx_INT_TYPE`¹,² | Wakeup is generated when | Wakeup is cleared when |
| :----------------------- | :------------------------ | :---------------------- |
| 5                        | the input GPIO is high-level. | the input GPIO is low-level. |
| 4                        | the input GPIO is low-level. | the input GPIO is high-level. |

¹ x ranges from 0 to 54.
² If the register is configured to any other value, HP GPIO wakeup feature is disabled.

### 9.4.6.2 LP GPIO Wakeup

The LP GPIO wakeup feature is designed to awaken the system from Deep-sleep when the LP peripherals are not in power gating mode. LP GPIO wakeup is not available when the LP peripherals are powered down.

GPIO0 ~ GPIO15 can be used to generate LP GPIO wakeup by enabling `LP_GPIO_PINn_WAKEUP_ENABLE` (n: 0 ~ 15).

LP GPIO wakeup supports posedge sensitive, negedge sensitive, both posedge and negedge sensitive, high-voltage sensitive and low-voltage sensitive wakeups, with specific conditions based on the GPIO configuration.
```