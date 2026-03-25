

```markdown
The LP PD Peripherals domain can only be powered up and down while the PMU state switches between HP_SLEEP and LP_SLEEP PMU. The other power domains can be powered up and down while the PMU states switch between HP_SLEEP, HP_ACTIVE, and HP_MODEM.

When the chip switches between PMU states, if the power configuration of a power domain in the current PMU state does not match the power configuration it is about to switch to, then the power up-down process will be activated. Take the power up-to-down process of the CPU power domain as an example. Configure `PMU_HP_MODEM_PD_HP_CPU_PD_EN` to 1 or 0 to indicate that the CPU power domain is powered down or up in the HP_MODEM state. PMU will perform the following configurations:

*   Enable the digital isolation unit to ensure that the powered-down modules do not output unstable voltage levels to the powered-up modules. When a power domain loses power, the output of this module will be clamped to a fixed value.
*   Enable reset. When the CPU power domain loses power, its global reset signal is set to a reset state, which persists for a period after the CPU power domain is re-powered. This mechanism guarantees a reset-to-release process for the CPU power domain during power-up, effectively mitigating any instability caused by power up-down transitions.

The following explains the power up and down of each digital power domain:

*   Internal SRAMx

    The power up and down of the Internal SRAMx domain is not controlled by a dedicated register. The Internal SRAMx domain shares the `PMU_PMUSTATE_PD_TOP_PD_EN` register with the Peripherals domain. If `PMU_PD_HP_MEMn_PD_MASK (n=0,1,2)` is 0, both the Internal SRAMx and Peripherals power domains are powered up or down simultaneously. If `PMU_PD_HP_MEMn_PD_MASK` is 1, the Internal SRAMx can remain powered up when the Peripherals domain is powered down.

*   Modem Power

    Modem Power is connected to the HP sys regulator through a power switch.
    `PMU_HP_ACTIVE_PD_HP_AON_PD_EN` controls its power up and down in HP_ACTIVE state. From Figure 13.4-1, it can be seen that if any of the CPU, Modem, or Peripherals + ROM power domains needs to be powered up, the Modem Power domain must also be powered up. Such a design meets functional requirements.

*   Peripherals + ROM/Modem/CPU:

    Each of the three power domains can be powered up and down in different PMU states using the `PMU_PMUSTATE_PD_n_PD_EN` register (`n=TOP/HP_WIFI/HP_CPU`). “WIFI” in the register represents the Modem Power domain.

When the Peripherals domain is powered down, the following features are configurable:

    -   Powering down the Peripherals domain may cause instability in GPIOs. This can be addressed by maintaining the state of the GPIOs (excluding eight LP GPIOs) through PMU. For example, configuring `PMU_HP_SLEEP_HP_PAD_HOLD_ALL` keeps GPIOs in the same state as before Peripherals was powered down in HP_SLEEP.
    -   In HP_ACTIVE and HP_MODEM states, the Internal SRAMx domain can be powered down or put into Deep-sleep mode. In Deep-sleep, the memory cannot be read or written to, but data can be retained. Configure `PMU_PMUSTATE_HP_MEM_DSLP` to enable Memory Deep-sleep mode.
```