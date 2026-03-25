

```markdown
Chapter 8 GPIO Matrix and IO MUX

GoBack

1 x ranges from O to 14, 23 to 28.
2 If the field is configured to any other value, HP GPIO wakeup feature is disabled.

8.4.6.2 LP GPIO Wakeup

The LP GPIO wakeup feature is designed to awaken the system from Deep-sleep. LP GPIO wakeup is not available when the LP peripherals are powered down.

GPIO0~GPIO6 can be used to generate LP GPIO wakeup by enabling LP_GPIO_PINx_WAKEUP_ENABLE (x: 0~6).

LP GPIO wakeup supports the following types, depending on the configuration of
LP_GPIO_PINx_INT_TYPE:

- posedge sensitive
- negedge sensitive
- both posedge and negedge sensitive
- high-voltage sensitive and low-voltage sensitive

Table 8.4-2. LP GPIO Wakeup Signal Trigger and Clear Conditions

| LP_GPIO_PINx_INT_TYPE¹,² | Wakeup is generated when                                                                 | Wakeup is cleared when                                      |
|--------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 1                        | GPIO input toggles from low-level to high-level                                         | LP_GPIO_PINx_EDGE_WAKEUP_CLR is set                         |
| 2                        | GPIO input toggles from high-level to low-level                                        | LP_GPIO_PINx_EDGE_WAKEUP_CLR is set                         |
| 3                        | GPIO input toggles from high-level to low-level, or vice versa                           | LP_GPIO_PINx_EDGE_WAKEUP_CLR is set                         |
| 4                        | GPIO input is low-level                                                                  | GPIO input is high-level                                    |
| 5                        | GPIO input is high-level                                                                 | GPIO input is low-level                                     |

¹ x ranges from O to 6.
² If the field is configured to any other value, LP GPIO wakeup feature is disabled.

8.4.7 Programming Procedure

8.4.7.1 HP GPIO Matrix

To read GPIO pin X¹ into HP peripheral signal Y, follow the steps below:

1. Configure GPIO_FUNCy_IN_SEL_CFG_REG corresponding to HP peripheral signal Y in HP GPIO matrix:
   - Set GPIO_SIGy_IN_SEL to enable peripheral signal input via HP GPIO matrix.
   - Set GPIO_FUNCy_IN_SEL to the desired GPIO pin, i.e., X here.

Note: some peripheral signals have no valid GPIO_SIGy_IN_SEL bit, namely, these peripherals can only receive input signals via HP GPIO matrix.

2. Optionally enable the GPIO Filter for pin input signals by setting IO_MUX_GPIOx_FILTER_EN.

3. Enable Glitch Filter feature as follows:

Espressif Systems
Submit Documentation Feedback
ESP32-C5 TRM (Version 1.0)
```