

```markdown
- LP PD Peripherals

The LP PD Peripherals power domain remains powered up when the chip is in HP_ACTIVE and HP_MODEM states. The power state of LP PD Peripherals is configurable only in HP_SLEEP and LP_SLEEP states. The LP PD Peripherals power domain has an independent digital power switch, and its power control is not dependent on the power state of other digital power domains.

13.4.2.5 Clock Controller

The clock controller mainly controls the high-performance system clocks and LP system clocks when the chip switches between PMU states.

The high-performance system clocks include HP_ROOT_CLK and high-performance system peripherals clocks. When the chip switches between HP_ACTIVE, HP_MODEM, and HP_SLEEP states, PMU can switch, power up/down, and divide the frequency of HP_ROOT_CLK, as well as power up/down high-performance system peripherals clocks.

- HP_ROOT_CLK can be controlled as follows:

  - Configure `PMU_PMUSTATE_SYS_CLK_SLP_SEL` to select PMU to control the clock source of HP_ROOT_CLK in corresponding PMU state.
  
  - Configure `PMU_PMUSTATE_ICG_SYS_CLOCK_EN` to 0 to disable HP_ROOT_CLK in the corresponding PMU state.

  - Configure `PMU_PMUSTATE_DIG_SYS_CLK_SEL` to select the clock source of HP_ROOT_CLK in corresponding PMU state. For details, please refer to Chapter 9 Reset and Clock > Table 9.2-1.

- High-performance system peripheral clocks can be controlled as follows:

  - Configure `PMU_PMUSTATE_ICG_SLP_SEL` to 1 so that the clock gating in the target state is controlled by PMU. Configure this register to 0 so that the clock gating is controlled by PCR registers.

  - Configure `PMU_PMUSTATE_DIG_ICG_FUNC_EN` to power up or down the function clock in the target PMU state. For detailed configuration please see Chapter 9 Reset and Clock > Table 9.2-8.

  - Configure `PMU_PMUSTATE_DIG_ICG_APB_EN` to power up/down the APB clock in the target PMU state. For detailed configuration please see Chapter 9 Reset and Clock > Table 9.2-7.

The LP system clocks are mainly used in the low-power system and include the following clocks:

* LP_SLOW_CLK
* LP_FAST_CLK
* LP_DYN_SLOW_CLK
* LP_DYN_FAST_CLK

The clock frequency of LP_DYN_FAST_CLK is controlled by hardware, depending on the PMU state (and cannot be changed by the user):

* In LP_SLEEP state: The LP_DYN_FAST_CLK frequency is the same as LP_SLOW_CLK.
* In HP_ACTIVE/HP_MODEM/HP_SLEEP state: The LP_DYN_FAST_CLK frequency is the same as LP_FAST_CLK.
```