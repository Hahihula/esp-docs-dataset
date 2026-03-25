

```markdown
- Set IO_MUX_GPIO`n`_HYS_EN to enable the hysteresis function for GPIO`n`.
- Clear IO_MUX_GPIO`n`_HYS_EN to disable the hysteresis function for GPIO`n`.

Recommended Operation:

*   Set IO_MUX_GPIO`n`_HYS_SEL.
*   Then enable or disable the hysteresis function for GPIO`n` using IO_MUX_GPIO`n`_HYS_EN.

## 8.11 Power Supplies and Management of GPIO Pins

### 8.11.1 Power Supplies of GPIO Pins

For more information on the power supply for GPIO pins, please refer to Pin Definition in ESP32-C5 Datasheet. All the pins can be used to wake up the chip from Light-sleep, but only the pins (GPIO0~GPIO6) in VDDPST1 domain can be used to wake up the chip from Deep-sleep.

### 8.11.2 Power Supply Management

Each ESP32-C5 pin is connected to one of the following power domains.
*   VDDPST1: the input power supply for LP GPIO pins
*   VDDPST2: the input power supply for HP GPIO pins

## 8.12 HP Peripheral Signal List

Table 8.12-1 shows the peripheral input/output signals via HP GPIO matrix.

Please pay attention to the configuration of the bit `GPIO_FUNC`n`_OE_SEL`:

*   `GPIO_FUNC`n`_OE_SEL = 1`: the output enable is controlled by the corresponding bit `n` of `GPIO_ENABLE_REG`:
    -   `GPIO_ENABLE_REG = 0`: output is disabled.
    -   `GPIO_ENABLE_REG = 1`: output is enabled.
*   `GPIO_FUNC`n`_OE_SEL = 0`: use the output enable signal from peripheral, for example SPIQ_oE in the column "Output enable signal when GPIO_FUNC`n`_OE_SEL = 0" of Table 8.12-1. Note that the signals such as SPIQ_oE can be 1 ('1'd1) or 0 ('1'd0), depending on the configuration of corresponding peripherals. If it's 1'd1 in column "Output enable signal when GPIO_FUNC`n`_OE_SEL = 0", it indicates that once `GPIO_FUNC`n`_OE_SEL` is cleared, the output signal is always enabled by default.

**Note:**
Signals are numbered consecutively, but not all signals are valid.
*   Only the signals with a name assigned in the column "Input signal" in Table 8.12-1 are valid input signals.
*   Only the signals with a name assigned in the column "Output signal" in Table 8.12-1 are valid output signals.
```