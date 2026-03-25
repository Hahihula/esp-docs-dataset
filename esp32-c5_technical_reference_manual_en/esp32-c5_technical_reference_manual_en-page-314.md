

```markdown
Note:
Not all signals can be directly connected to peripheral via IO MUX. Some input/output signals can only be connected to peripheral via GPIO matrix. See Table 8.12-1.
```

## 8.7 Analog Functions

### 8.7.1 Overview

ESP32-C5 provides 11 GPIO pins (GPIO0~GPIO6, GPIO8~GPIO9, GPIO13~GPIO14) with analog functions, including 6 LP GPIO pins and 5 HP GPIO pins. See Table 8.15-1.

### 8.7.2 Analog Functions

When the pin is used for analog purpose, make sure this pin is left floating by configuring registers. By such way, the external analog signal is directly connected to internal analog signal via GPIO pin. The configuration is as follows:

*   Clear `IO_MUX_GPIO{n}_FUN_IE`, `IO_MUX_GPIO{n}_FUN_WPU`, and `IO_MUX_GPIO{n}_FUN_WPD`, to set the pin floating.
*   Write 1 to the corresponding bit in `GPIO_ENABLE_W1TC`, to clear output enable.

To use these functions listed in Table 8.15-1, please refer to the following related chapters:

*   For XTAL_32K related functions, see Chapter 13 Low-Power Management.
*   For ADC related functions, see Chapter 46 ADC Controller.
*   For voltage comparator related functions, see Chapter 47 Analog Voltage Comparator.

Note:
GPIO1 has two different analog functions, which can be used simultaneously.

## 8.8 Pin Functions in Light-sleep

Pins may provide different functions when ESP32-C5 is in Light-sleep mode. If `IO_MUX_GPIO{n}_SLP_SEL` in register `IO_MUX_GPIO{n}_REG` for a GPIO pin is set to 1, a different set of bits will be used to control the pin when the chip is in Light-sleep mode.

Table 8.8-1. Bit Used to Control IO MUX Functions in Light-sleep Mode

| IO MUX Function | Normal Execution OR `IO_MUX_GPIO{n}_SLP_SEL = 0` | Light-sleep Mode AND `IO_MUX_GPIO{n}_SLP_SEL = 1` |
|------------------|--------------------------------------------------|---------------------------------------------------|
| Output Drive Strength | `IO_MUX_GPIO{n}_FUN_DRV`                        | `IO_MUX_GPIO{n}_MCU_DRV`                          |
| Pull-up Resistor   | `IO_MUX_GPIO{n}_FUN_WPU`                         | `IO_MUX_GPIO{n}_MCU_WPU`                           |
| Pull-down Resistor | `IO_MUX_GPIO{n}_FUN_WPD`                         | `IO_MUX_GPIO{n}_MCU_WPD`                           |

Cont’d on next page
```