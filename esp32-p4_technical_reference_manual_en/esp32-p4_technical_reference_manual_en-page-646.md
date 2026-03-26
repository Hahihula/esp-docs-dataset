

```markdown
→ SYS_CLK → MEM_CLK → CPU_CLK. When switching from a low divisor to a high divisor, the recommended configuration order is CPU_CLK → MEM_CLK → SYS_CLK → APB_CLK. This helps to prevent high-frequency clock glitches.
```

### 10.3.2 LP System Clock Configuration

* Configure the clock source of LP_SLOW_CLK via `LP_CLKRST_SLOW_CLK_SEL`
* Configure the clock source of LP_FAST_CLK via `LP_CLKRST_FAST_CLK_SEL`
* Configure the clock divisor of LP_PERI_CLK via `LP_CLKRST_LP_PERI_DIV_NUM`

### 10.3.3 Peripheral Clock Reset and Configuration

**Notice:**

ESP32-P4 features low power consumption. This is why some peripheral clocks are gated (disabled) by default. Before using any of these peripherals, it is mandatory to enable the clock for the given peripheral by setting the corresponding `CLK_EN` bit to 1, and release the peripheral from the reset state to make it operational by setting the `RST_EN` bit to 0.

The clocks of most peripherals can be classified into two types:

* Bus clock: used to configure peripheral registers.
* Function clock: such as UART’s reference clock, used by peripherals to operate.

The function clock of most peripherals can be selected from multiple clock sources. In the description of the gating registers, it will be stated whether a register is a bus clock (SYS_CLK, APB_CLK) gating register or a function clock gating register.

Bus clock enable/disable registers, function clock enable/disable registers, clock source selection registers, and clock frequency division registers are grouped into the `HP_SYS_CLKRST`, `LP_CLKRST`, and `LPPERI` modules. Except for EMA, SDMMAC, USB Serial/JTAG, Full-Speed USB 2.0 OTG, and High-Speed USB 2.0 OTG, whose reset configuration registers are in the `LP_CLKRST` module, all the other HP clock and reset registers are in the `HP_SYS_CLKRST` module. For more information, see Section 10.4 Register Summary.

When changing the clock configuration, it is recommended to turn off the corresponding clock gate first, update the clock divider configurations, clock sources, and other configurations, and then turn it on again.

When a peripheral is not working, users can turn off its function clock by configuring related registers. Turning off the peripheral’s function clock does not affect the rest of the system.

Take I2C clock configuration as an example.
```