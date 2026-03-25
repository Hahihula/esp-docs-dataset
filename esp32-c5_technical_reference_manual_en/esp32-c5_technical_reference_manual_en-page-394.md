

```markdown
enable register to apply the new configuration. To check whether the new configuration takes effect, read PCR_BUS_CLOCK_UPDATE and see if it is 0.

## 9.3.2 LP System Clock Configuration

The clock source of LP_SLOW_CLK can be configured via `LP_CLKRST_SLOW_CLK_SEL`.

The clock source of LP_FAST_CLK can be configured via `LP_CLKRST_FAST_CLK_SEL`.

## 9.3.3 Peripheral Clock Reset and Configuration

**Notice:**

ESP32-C5 features low power consumption. This is why some peripheral clocks are gated (disabled) by default. Before using any of these peripherals, it is mandatory to enable the clock for the given peripheral by setting the corresponding CLK_EN bit to 1, and release the peripheral from reset state by setting the RST_EN bit to 0.

The clocks of most peripherals can be classified into two types:

*   Bus clock: used to configure peripheral registers.
*   Functional clock: such as UART’s reference clock, used by peripherals to operate.

The functional clock of most peripherals can be selected from multiple clock sources. For clock gating registers, whether they are used to gate the bus clock (AHB_CLK, APB_CLK) or the functional clock will be stated in the corresponding register descriptions.

Bus clock switches, functional clock switches, and configuration registers for clock source selection and clock frequency division are grouped into the PCR module. For more information, see Section 9.4 Register Summary.

When a peripheral is not working, users can turn off its functional clock by configuring related PCR registers. Turning off the peripheral’s functional clock does not affect the rest of the system.

Take the I2C clock configuration as an example.
```

![Figure 9.3-1. Clock Configuration Example](image)

**Figure 9.3-1. Clock Configuration Example**
```