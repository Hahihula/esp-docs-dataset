

```markdown
PMU will perform the following configurations:

* Enable the digital isolation unit to ensure that the powered-down modules do not output unstable voltage levels to the powered-up modules. When a power domain loses power, the output of this module will be clamped to a fixed value.
* Enable reset. When the CPU power domain loses power, its global reset signal is set to a reset state, which persists for a period after the CPU power domain is re-powered. This mechanism guarantees a reset-to-release process for the CPU power domain during power-up, effectively mitigating any instability caused by power up-down transitions.

The following will explain the power up and down of each digital power domain:

* Internal SRAMx

  The Internal SRAMx power domain and “ROM + Peripherals” power domain share the same control register PMU_PMUSTATE_PD_TOP_PD_EN. The PMU_PD_HP_MEMx_PD_MASK (x=0,1,2) configures whether Internal SRAMx will power on/off simultaneously with the HPTOP power domain:

  - 0: powers on/off simultaneously with the “ROM + Peripherals” power domain.
  - 1: does not power on/off simultaneously with the “ROM + Peripherals” power domain. In this case, users can configure PMU_PD_HP_MEMx_PD_MASK (x=0,1,2) to keep Internal SRAMx powered on even when the “ROM + Peripherals” power domain is powered off.

* Modem Power

  Modem Power is connected to the HP system regulator through a power switch. The power up and down of Modem Power in different PMU state is determined by PMU_PMUSTATE_PD_HP_AON_PD_EN (PMUSTATE=HP_ACTIVE/HP_MODEM/HP_SLEEP). From Figure 11.4-1, it can be seen that if any of the CPU, Modem, or “ROM + Peripherals” power domains needs to be powered up, the Modem Power domain must also be powered up. Such a design meets functional requirements.

* “ROM + Peripherals”, Modem and CPU

  Each of the three power domains can be powered up and down in different PMU states using register PMU_POWERDOMAIN_PD_PMUSTATE_PD_EN(POWERDOMAIN=TOP/HP_WIFI/HP_CPU) respectively.

  When the “ROM + Peripherals” domain is powered down, the following features are configurable:

  - Powering down the “ROM + Peripherals” domain may cause instability in GPIOs. This can be addressed by maintaining the state of the GPIOs (excluding eight LP GPIOs) through PMU. For example, configuring PMU_HP_SLEEP_HP_PAD_HOLD_ALL can keep GPIOs in the same state as before “ROM + Peripherals” was powered down in HP_SLEEP.
  - In HP_ACTIVE, HP_SLEEP and HP_MODEM states, the Internal SRAMx domain can be powered down or put into Deep-sleep mode. In Deep-sleep, the memory cannot be read or written to, but data can be retained. Configure PMU_PMUSTATE_HP_MEM_DSLP to enable Memory Deep-sleep mode.

* LPSYS_OFF

  The LPSYS_OFF power domain remains powered up when the chip is in HP_ACTIVE and HP_MODEM states. The power state of LPSYS_OFF is configurable only in HP_SLEEP and LP_SLEEP states via PMU_LP_SLEEP_LP_DIG_POWER_REG and PMU_HP_SLEEP_LP_DIG_POWER_REG respectively. The LPSYS_OFF power domain has an independent digital power switch, and its power control is not dependent on the power state of other digital power domains.
```