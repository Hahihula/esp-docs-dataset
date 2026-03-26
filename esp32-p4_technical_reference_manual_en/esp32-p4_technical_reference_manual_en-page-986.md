

```markdown
Chapter 14 Low-Power Management GoBack

The configuration of the regulators is as follows:

*   Configure PMU_n1_HP_REGULATOR_XPD or PMU_n1_LP_REGULATOR_XPD to enable or disable the output voltage of the HP/LP sys regulator in the target PMU state. Turning off the LP sys regulator is not recommended, as it may cause the PMU itself to power down, resulting in chip malfunction.

The configuration of the high-speed clocks (XTAL_CLK and PLL clocks) is as follows:

*   XTAL_CLK: Configure PMU_HP_SLEEP_XPD_XTAL to 1 to enable XTAL_CLK when the chip switches the PMU state to HP_SLEEP.
    Note: To avoid the instability in XTAL_CLK during startup, users have the option to configure PMU_WAIT_XTL_STABLE to delay the gate opening for XTAL_CLK. This delay ensures that the gate opening is enabled after PMU_WAIT_XTL_STABLE CLK_DYN_FAST_CLK cycles following the power-up of XTAL_CLK.

*   CPLL_CLK: PMU can enable CPLL_CLK in different PMU states by configuring PMU_n1_XPD_PLL[0] to 1. For example, configuring PMU_HP_ACTIVE_XD_PLL[0] to 1 enables the CPLL_CLK clock when the chip is in HP_ACTIVE state.

*   SPLL_CLK: PMU can enable SPLL_CLK in different PMU states by configuring PMU_n1_XPD_PLL[1] to 1. For example, configuring PMU_HP_ACTIVE_XPD_PLL[1] to 1 enables the SPLL_CLK clock when the chip is in HP_ACTIVE state.

*   Audio PLL: PMU can enable Audio PLL in different PMU states by configuring PMU_n1_XPD_PLL[2] to 1. For example, configuring PMU_HP_ACTIVE_XPD_PLL[2] to 1 enables the Audio PLL clock when the chip is in HP_ACTIVE state.

*   SDIO PLL: PMU can enable SDIO PLL in different PMU states by configuring PMU_n1_XPD_PLL[3] to 1. For example, configuring PMU_HP_ACTIVE_XPD_PLL[3] to 1 enables the SDIO PLL clock when the chip is in HP_ACTIVE state.

Note:

-   Before enabling the PLL clocks please ensure that XTAL_CLK is stable.
-   To avoid the instability in the PLL clocks during startup, users have the option to configure PMU_WAIT_PLL_STABLE to delay the gate opening for the PLL clocks. This delay ensures that the gate opening is enabled after PMU_WAIT_PLL_STABLE CLK_DYN_FAST_CLK cycles following the power-up of the PLL clocks.

Slow-speed clocks (RC_FAST_CLK and XTAL32K_CLK) operate with low power. The power up and down of the slow-speed clocks in HP_ACTIVE and HP_SLEEP states are controlled by PMU_HP_SLEEP_XPD_FOSC_CLK. In LP_SLEEP state, the power up and down of the slow-speed clocks are controlled by PMU_LP_SLEEP_XPD_FOSC_CLK.

14.4.2.4 Digital Power Controller

The digital power controller controls the power up and down of digital power domains in different PMU states. Unlike the analog power controller, the digital power controller does not directly control the regulator but instead controls the power switch connected to the regulator to power up and down the digital power domains.

The LP PD Peripherals domain can only be powered up and down while the PMU state switches between
```