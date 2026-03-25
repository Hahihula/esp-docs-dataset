

```markdown
- LP always-on (LPSYS)

LPSYS includes modules such as the PMU that will not power down unless the chip is completely powered off. Therefore, the power on/off state of this power domain cannot be configured.

11.4.2.5 Clock Controller

The clock controller is mainly used to select, enable and configure high-performance system clocks and low-power system clocks when the chip switches between PMU states.

High-performance system clocks include HP_ROOT_CLK and high-performance system peripherals clocks. When the chip switches among HP_ACTIVE, HP_MODEM, and HP_SLEEP states, PMU can switch, power up/down, and divide the frequency of HP_ROOT_CLK, as well as power up/down high-performance system peripherals clocks.

- HP_ROOT_CLK can be controlled as follows:

  - Configure `PMU_PMUSTATE_SYS_CLK_SLP_SEL` to 1 to indicate that when the chip enters the corresponding PMU state, the clock source is controlled by PMU.
  
  - Configure `PMU_PMUSTATE_ICG_SYS_CLOCK_EN` to 0 to disable HP_ROOT_CLK in the corresponding PMU state.

  - Configure `PMU_PMUSTATE_DIG_SYS_CLK_SEL` to select the clock source after the chip enters the corresponding PMU state. For details, please refer to Chapter 7 Reset and Clock > Table 7.2-1.

- High-performance system peripheral clocks can be controlled as follows:

  - Configure `PMU_PMUSTATE_ICG_SLP_SEL` to 1 so that the clock gating in the target state will be controlled by PMU. Configure this register to 0 so that the clock gating is controlled by PCR registers.
  
  - Configure `PMU_PMUSTATE_DIG_ICG_FUNC_EN` to power up/down the function clock in the target PMU state. For detailed configuration please see Chapter 7 Reset and Clock > Table 7.2-8.

  - Configure `PMU_PMUSTATE_DIG_ICG_APB_EN` to power up/down the APB clock in the target PMU state. For detailed configuration please see Chapter 7 Reset and Clock > Table 7.2-7.

LP system clocks are mainly used in the low-power system and include the following four clocks:

- LP_SLOW_CLK
- LP_FAST_CLK
- LP_DYN_SLOW_CLK
- LP_DYN_FAST_CLK

The clock frequencies of LP_DYN_FAST_CLK and LP_DYN_SLOW_CLK are controlled by hardware as follows, depending on the PMU state (and cannot be changed by the user):

- LP_SLEEP: The frequency of LP_DYN_FAST_CLK and LP_DYN_SLOW_CLK is the same as LP_SLOW_CLK.
  
- HP_ACTIVE, HP_MODEM, HP_SLEEP:

  - The LP_DYN_FAST_CLK frequency is the same as LP_FAST_CLK.
```