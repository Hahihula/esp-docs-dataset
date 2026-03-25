

```markdown
- XTAL_CLK: Configure `PMU_HP_SLEEP_XPD_XTAL` to 1 to enable XTAL_CLK when the chip switches PMU state to HP_SLEEP.

Note: To avoid the instability in XTAL_CLK during startup, users have the option to configure `PMU_WAIT_XTAL_STABLE` to delay the gate opening for XTAL_CLK. This delay ensures that the gate opening is enabled after `PMU_WAIT_XTAL_STABLE CLK_DYN_FAST_CLK` cycles following the power-up of XTAL_CLK.

- PLL_CLK: PMU can enable PLL_CLK in different PMU states by configuring `PMU_m1_XPD_BBPLL` to 1. For example, configuring `PMU_HP_ACTIVE_XPD_BBPLL` to 1 will enable the PLL_CLK clock when the chip is in HP_ACTIVE state.

Note:
- Before enabling PLL_CLK please ensure that XTAL_CLK is stable.
- To avoid the instability in PLL_CLK during startup, users have the option to configure `PMU_WAIT_PLL_STABLE` to delay the gate opening for PLL_CLK. This delay ensures that the gate opening is enabled after `CLK_DYN_FAST_CLK` cycles in the number of `PMU_WAIT_PLL_STABLE` following the power-up of PLL_CLK.

The slow-speed clocks (RC_FAST_CLK and XTAL32K_CLK) operate with low power. In HP_ACTIVE and HP_SLEEP states, the power up and down of the slow-speed clocks are controlled by `PMU_HP_SLEEP_LP_CK_POWER_REG`. In LP_SLEEP state, the power up and down of the slow-speed clocks are controlled by `PMU_LP_SLEEP_LP_CK_POWER_REG`.

### 11.4.2.4 Digital Power Controller

The digital power controller controls the power up and down of digital power domains in different PMU states. Unlike the analog power controller, the digital power controller does not directly control the regulator but instead controls the power switch connected to the regulator to power up and down the digital power domains.

The digital power domains can be powered up and down while the PMU states switch between HP_SLEEP and HP_ACTIVE states.

When the chip switches between PMU states, if the power configuration of a power domain in the current PMU state does not match the power configuration it is about to switch to, then the power up-down process will be activated. Take the power up-to-down process of the CPU power domain as an example. Configure `PMU_HP_SLEEP_PD_HP_CPU_PD_EN` to 1 or 0 to indicate that the CPU power domain is powered down or up in the HP_SLEEP state. PMU will perform the following configurations:

- Enable the digital isolation unit to ensure that the powered-down modules do not output unstable voltage levels to the powered-up modules. When a power domain loses power, the output of this module will be clamped to a fixed value.
- Enable reset. When the CPU power domain loses power, its global reset signal is set to a reset state, which persists for a period after the CPU power domain is re-powered. This mechanism guarantees a reset-to-release process for the CPU power domain during power-up, effectively mitigating any instability caused by power up-down transitions.

The following will explain the power up and down of each digital power domain:

- Internal SRAMx
```