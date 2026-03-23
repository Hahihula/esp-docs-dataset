

```markdown
- If XTAL_CLK or RC_FAST_CLK is selected as the clock source of HP_ROOT_CLK,
  - the clock divisor for CPU_CLK can be configured via `PCR_CPU_LS_DIV_NUM`.
  - the clock divisor for AHB_CLK can be configured via `PCR_AHB_LS_DIV_NUM`.

## 8.3.2 LP System Clock Configuration

The clock source of LP_SLOW_CLK can be configured via `LP_CLKRST_SLOW_CLK_SEL`.

The clock source of LP_FAST_CLK can be configured via `LP_CLKRST_FAST_CLK_SEL`.

## 8.3.3 Peripheral Clock Reset and Configuration

**Notice:**
ESP32-C6 features low power consumption. This is why some peripheral clocks are gated (disabled) by default. Before using any of these peripherals, it is mandatory to enable the clock for the given peripheral by setting the corresponding `CLK_EN` bit to 1, and release the peripheral from reset state to make it operational by setting the `RST_EN` bit to 0.

The clocks of most peripherals can be classified into two types:
* Bus clock: used to configure peripheral registers.
* Function clock: such as UART’s reference clock, used by peripherals to operate.

The operating clock (function clock) of most peripherals can be selected from multiple clock sources. In the description of the gating registers, it will be stated whether the register belongs to the bus clock (`AHB_CLK`, `APB_CLK`) gating register or the function clock gating register.

Bus clock switches, function clock switches, and the configuration registers for clock source selection and clock frequency division are grouped into the PCR module. For more information, see Section 8.4 Register Summary.

When a peripheral is not working, users can turn off its function clock by configuring related registers. Turning off the peripheral’s function clock does not affect the rest of the system.

Take I2C clock configuration as an example.
```