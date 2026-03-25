

```markdown
Note: To avoid the instability in XTL_CLK during startup, users have the option to configure PMU_WAIT_XTL_STABLE to delay the gate opening for XTL_CLK. This delay ensures that the gate opening is enabled after PMU_WAIT_XTL_STABLE cycles in CLK_DYN_FAST_CLK following the power-up of XTL_CLK.

* PLL_CLK: PMU can enable PLL_CLK in different PMU states by configuring PMU_PMUSTATE_XPD_BBPLL to 1. For example, configuring PMU_HP_ACTIVE_XPD_BBPLL to 1 will enable the PLL_CLK clock when the chip is in HP_ACTIVE state.

Note:
- Before enabling PLL_CLK, please ensure that XTL_CLK is stable.
- To avoid the instability in PLL_CLK during startup, users have the option to configure PMU_WAIT_PLL_STABLE to delay the gate opening for PLL_CLK. This delay ensures that the gate opening is enabled after PMU_WAIT_PLL_STABLE cycles in CLK_DYN_FAST_CLK following the power-up of PLL_CLK.

Slow-speed clocks include:

* RC_FAST_CLK
* XTL32K_CLK
* RC32K_CLK
* SOSC_CLK

These slow-speed clocks operate with low power. The power up and down of these clocks in different PMU states is configured via different registers. Take RC_FAST_CLK as an example:

* HP_ACTIVE, HP_MODEM and HP_SLEEP: PMU_HP_SLEEP_XPD_FOSC_CLK
* LP_SLEEP: PMU_LP_SLEEP_XPD_FOSC_CLK

### 11.4.2.4 Digital Power Controller

The digital power controller controls the power up and down of digital power domains in different PMU states. Unlike the analog power controller, the digital power controller does not directly control the regulator but instead controls the power switch connected to the regulator to power up and down the digital power domains.

Among the digital power domains, the LPSYS_OFF domain can only be powered up and down during the PMU state switch between HP_SLEEP and LP_SLEEP PMU, while the other power domains can be powered up and down during the PMU states switch among HP_SLEEP, HP_ACTIVE, and HP_MODEM.

When the chip switches between PMU states, if the power configuration of a power domain in the current PMU state does not match the power configuration it is about to switch to, then the power up-down process will be activated.

Take the power up-to-down process of the CPU power domain as an example. Configure PMU_HP_MODEM_PD_HP_CPU_PD_EN:

* 0: indicates that the CPU power domain is powered up in the HP_MODEM state.
* 1: indicates that the CPU power domain is powered down in the HP_MODEM state.
```