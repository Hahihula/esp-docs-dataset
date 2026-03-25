

```markdown
PLL_F96M_CLK

PLL_F96M_CLK is a 96 MHz clock. PLL_F48M_CLK (48 MHz) is divided from PLL_F96M_CLK.

CRYPTO_CLK

As shown in Figure 7.2-3, CRYPTO_CLK can be derived from XTAL_CLK, PLL_96M_CLK, PLL_64M_CLK, or RC_FAST_CLK, and its frequency is up to 96 MHz.

To protect encryption and decryption peripherals from DPA (Differential Power Analysis) attacks, a random divider strategy is implemented for the functional clock of encryption and decryption peripherals. Three security levels are available, depending on the range of random divider. Users can select the security level by configuring HP_SYSTEM_SEC_DPA_CONF_REG. If HP_SYSTEM_SEC_DPA_CFG_SEL is set to 1, the security level is determined by the configuration of EFUSE_SEC_DPA_LEVEL, otherwise, by the value of HP_SYSTEM_SEC_DPA_LEVEL.

LED_PWM Clock

LEDC module uses PLL_F96M_CLK, RC_FAST_CLK or XTAL_CLK as its clock source. When the system is in low-power mode (APB_CLK is disabled), most peripherals are halted, but LEDC can still work via RC_FAST_CLK.
```

## 7.3 Programming Procedures

### 7.3.1 HP System Clock Configuration

When configuring `PCR_SOC_CLK_SEL` to select the clock source of `HP_ROOT_CLK`, or configuring the clock divisor for `CPU_CLK` via `PCR_CPU_DIV_NUM` and `AHB_CLK` via `PCR_AHB_DIV_NUM`, please also set the enable register to apply the new configuration. To check whether the new configuration takes effect, read `PCR_BUS_CLOCK_UPDATE` and see if it is 0.

### 7.3.2 LP System Clock Configuration

The clock source of `LP_SLOW_CLK` can be configured via `LP_CLKRST_SLOW_CLK_SEL`.

The clock source of `LP_FAST_CLK` can be configured via `LP_CLKRST_FAST_CLK_SEL`.

### 7.3.3 Peripheral Clock Reset and Configuration

**Notice:**

ESP32-H2 features low power consumption. This is why some peripheral clocks are gated (disabled) by default. Before using any of these peripherals, it is mandatory to enable the clock for the given peripheral by setting the corresponding `CLK_EN` bit to 1, and release the peripheral from reset state to make it operational by setting the `RST_EN` bit to 0.

The clocks of most peripherals can be classified into two types:

* Bus clock: used to configure peripheral registers.
* Functional clock: such as UART’s reference clock, used by peripherals to operate.
```