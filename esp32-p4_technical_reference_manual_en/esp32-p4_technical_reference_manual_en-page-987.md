

```markdown
HP_SLEEP and LP_SLEEP. The other digital power domains can only be powered up and down while the PMU state switches between HP_SLEEP and HP_ACTIVE.

When the chip switches between PMU states, if the power configuration of a power domain in the current PMU state does not match the power configuration it is about to switch to, then the power up-down process will be activated. Take the power up-to-down process of the CPU power domain as an example. Configure `PMU_HP_SLEEP_PD_TOP_PD_EN` to 1 or 0 to power down or up the CPU power domain in HP_SLEEP. PMU will perform the following configurations:

* Enable the digital isolation unit to ensure that the powered-down modules do not output unstable voltage levels to the powered-up modules. When a power domain loses power, the output of this module will be clamped to a fixed value.
* Enable reset. When the CPU power domain loses power, its global reset signal is set to a reset state, which persists for a period after the CPU power domain is re-powered. This mechanism guarantees a reset-to-release process for the CPU power domain during power-up, effectively mitigating any instability caused by power up-down transitions.

The following explains the power up and down of each digital power domain:

* L2MEM_GO–G5
  Configure `PMU_n1_PD_HP_MEM_PD_EN` to power up or down L2MEM_GO–G5.
* HP_CNNT
  Configure `PMU_n1_PD_CNNT_PD_EN` to power up or down HP_CNNT.
* PD_HP_CPU
  Configure `PMU_n1_PD_HP_CPU_PD_EN` to power up or down PD_HP_CPU.
* Peripherals + ROM (PD_TOP)
  Configure `PMU_n1_PD_TOP_PD_EN` to power or down PD_TOP.

When the Peripherals domain is powered down, the following features are configurable:

- Powering down the Peripherals domain may cause instability in GPIOs. This can be addressed by maintaining the state of the GPIOs (excluding the LP GPIOs) through PMU. For example, configuring `PMU_HP_SLEEP_HP_PAD_HOLD_ALL` can keep GPIOs in the same state as before Peripherals was powered down in HP_SLEEP.
- In the HP_ACTIVE state, Memory Deep-sleep mode is supported under a standard power supply. The memory cannot be read or written in this mode, but data can be retained. Configure `PMU_n1_HP_MEM_DSLP` to enable this mode.

* LP PD Peripherals

The LP PD Peripherals power domain remains powered up when the chip is in HP_ACTIVE state. The power state of LP PD Peripherals is configurable only in HP_SLEEP and LP_SLEEP states. The LP PD Peripherals power domain has an independent digital power switch, and its power control is not dependent on the power state of other digital power domains.
```