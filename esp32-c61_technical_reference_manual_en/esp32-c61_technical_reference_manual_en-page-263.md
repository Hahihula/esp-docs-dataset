

```markdown
## 6.7 Analog Functions

### 6.7.1 Overview

ESP32-C61 provides 9 GPIO pins (GPIO0~GPIO1, GPIO3~GPIO5, GPIO8~GPIO9, GPIO12~GPIO13) with analog functions, including 5 LP GPIO pins and 4 HP GPIO pins. See Table 6.15-1.

### 6.7.2 Analog Functions

When the pin is used for analog purpose, make sure this pin is left floating by configuring registers. By such way, the external analog signal is directly connected to internal analog signal via GPIO pin. The configuration is as follows:

* Clear `IO_MUX_GPIO{n}_FUN_IE`, `IO_MUX_GPIO{n}_FUN_WPU`, and `IO_MUX_GPIO{n}_FUN_WPD`, to set the pin floating.
* Write 1 to the corresponding bit in `GPIO_ENABLE_W1TC`, to clear output enable.

To use these functions listed in Table 6.15-1, please refer to the following related chapters:

* For XTAL_32K related functions, see Chapter 11 Low-Power Management.
* For ADC related functions, see Chapter 33 ADC Controller.
* For voltage comparator related functions, see Chapter 34 Analog Voltage Comparator.

## 6.8 Pin Functions in Light-sleep

Pins may provide different functions when ESP32-C61 is in Light-sleep mode. If `IO_MUX_GPIO{n}_SLP_SEL` register `IO_MUX_GPIO{n}_REG` for a GPIO pin is set to 1, a different set of bits will be used to control the pin when the chip is in Light-sleep mode.

Table 6.8-1. Bit Used to Control IO MUX Functions in Light-sleep Mode

| IO MUX Function | Normal Execution OR `IO_MUX_GPIO{n}_SLP_SEL = 0` | Light-sleep Mode AND `IO_MUX_GPIO{n}_SLP_SEL = 1 |
|------------------|--------------------------------------------------|-----------------------------------------------|
| Output Drive Strength | `IO_MUX_GPIO{n}_FUN_DRV`                        | `IO_MUX_GPIO{n}_MCU_DRV`                      |
| Pull-up Resistor    | `IO_MUX_GPIO{n}_FUN_WPU`                         | `IO_MUX_GPIO{n}_MCU_WPU`                      |
| Pull-down Resistor  | `IO_MUX_GPIO{n}_FUN_WPD`                         | `IO_MUX_GPIO{n}_MCU_WPD`                      |
| Input Enable        | `IO_MUX_GPIO{n}_FUN_IE`                          | `IO_MUX_GPIO{n}_MCU_IE`                       |
| Output Enable       | `OE_SEL from GPIO matrix*`                       | `IO_MUX_GPIO{n}_MCU_OE`                       |

\* If `IO_MUX_GPIO{n}_SLP_SEL` is set to 0, pin functions remain the same in both normal execution and in Light-sleep mode. Please refer to Section 6.5.3.1 for how to enable output in normal execution.
```