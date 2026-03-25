

```markdown
- Read the GPIO input from `GPIO_IN_REG[x]`.

For LP GPIO matrix, to implement simple GPIO input, follow the steps below:
- Set `LP_IOMUX_PADx_FUNC_IE` in `LP_IO_MUX_GPIOx_REG`, to enable pin input.
- Read the GPIO input from `LP_GPIO_IN_REG[x]`.
```

## 6.4.5 GPIO Wakeup

### 6.4.5.1 HP GPIO Wakeup

The HP GPIO wakeup feature is designed to awaken the system from Light-sleep. HP GPIO wakeup is not available when the HP system is powered down.

GPIO0~GPIO13 and GPIO22~GPIO29 can be used to generate HP GPIO wakeup by enabling `GPIO_PINx_WAKEUP_ENABLE` (x: 0~13, 22~29).

HP GPIO wakeup supports both high-voltage and low-voltage triggers, depending on the configuration of `GPIO_PINx_INT_TYPE`.

Table 6.4-1. HP GPIO Wakeup Signal Trigger and Clear Conditions

| `GPIO_PINx_INT_TYPE`¹,² | Wakeup is generated when | Wakeup is cleared when |
|-------------------------|----------------------------|--------------------------|
| 5                       | GPIO input is high-level   | GPIO input is low-level  |
| 4                       | GPIO input is low-level    | GPIO input is high-level |

¹ x ranges from 0 to 13, 22 to 29.
² If the field is configured to any other value, HP GPIO wakeup feature is disabled.

### 6.4.5.2 LP GPIO Wakeup

The LP GPIO wakeup feature is designed to awaken the system from Deep-sleep. LP GPIO wakeup is not available when the LP peripherals are powered down.

GPIO0~GPIO6 can be used to generate LP GPIO wakeup by enabling `LP_GPIO_PINx_WAKEUP_ENABLE` (x: 0~6).

LP GPIO wakeup supports the following types, depending on the configuration of `LP_GPIO_PINx_INT_TYPE`:

- posedge sensitive
- negedge sensitive
- both posedge and negedge sensitive
- high-voltage sensitive and low-voltage sensitive

Table 6.4-2. LP GPIO Wakeup Signal Trigger and Clear Conditions

| `LP_GPIO_PINx_INT_TYPE`¹,² | Wakeup is generated when | Wakeup is cleared when |
|----------------------------|----------------------------|--------------------------|
| 1                          | GPIO input toggles from low-level to high-level | `LP_GPIO_PINx_EDGE_WAKEUP_CLR` is set |
```