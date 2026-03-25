

```markdown
It is recommended to set IO_MUX_GPIO$n_HYS_SEL to 1, and use IO_MUX_GPIO$n_HYS_EN to enable or disable the hysteresis function of GPIO$n.

Figure 6.10-2. Example of level flip on the chip pad when the hysteresis function is enabled

## 6.11 Power Supplies and Management of GPIO Pins

### 6.11.1 Power Supplies of GPIO Pins

For more information on the power supply for GPIO pins, please refer to Pin Definition in ESP32-H2 Datasheet. All the pins can be used to wake up the chip from Light-sleep mode, but only the LP pins (GPIO8 ~ GPIO14) can be used to wake up the chip from Deep-sleep mode.

### 6.11.2 Power Supply Management

Each ESP32-H2 pin is connected to one of the three different power domains.
*   VDDPST1: the input power supply for some digital GPIOs and some LP GPIOs
*   VDDPST2: the input power supply for some digital GPIOs
*   VDDA_PMU/VBAT: the input power supply for GPIO12, XTAL_32K_P and XTAL_32K_N

## 6.12 Peripheral Signal List

Table 6.12-1 shows the peripheral input/output signals via GPIO matrix.

Please pay attention to the configuration of the bit GPIO_FUNC$n_OEN_SEL:

*   `GPIO_FUNC$n_OEN_SEL = 1`: the output enable is controlled by the corresponding bit $n$ of `GPIO_ENABLE_REG`:
    -   `GPIO_ENABLE_REG = 0`: output is disabled;
    -   `GPIO_ENABLE_REG = 1`: output is enabled;

*   `GPIO_FUNC$n_OEN_SEL = 0`: use the output enable signal from peripheral, for example SPIQ_oe in the column “Output enable signal when GPIO_FUNC$n_OEN_SEL = 0” of Table 6.12-1. Note that the signals such as SPIQ_oe can be 1 (1'd1) or 0 (1'd0), depending on the configuration of corresponding peripherals. If it's 1'd1 in column “Output enable signal when GPIO_FUNC$n_OEN_SEL = 0”, it indicates that once `GPIO_FUNC$n_OEN_SEL` is cleared, the output signal is always enabled by default.
```