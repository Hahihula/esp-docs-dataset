

```markdown
The power up and down of the Internal SRAMx domain is not controlled by a dedicated register. The Internal SRAMx domain shares the PMU_n1_PD_TOP_PD_EN register with the Peripherals domain. When PMU_PD_HP_MEMn_PD_MASK (n=1,2) is 0, both the Internal SRAMx and Peripherals power domains are turned up or down simultaneously. When PMU_PD_HP_MEMn_PD_MASK is 1, the Internal SRAMx can remain powered up when the Peripherals domain is powered down.

*   **Peripherals + ROM/Modem/CPU:**

    Each of the three power domains can be powered up and down in different PMU states using the PMU_n1_PD_n_PD_EN register (n=TOP/HP_CPU).

    When the Peripherals domain is powered down, the following features are configurable:

        -   Powering down the Peripherals domain may cause instability in GPIOs. This can be addressed by maintaining the state of the GPIOs (excluding the LP GPIOs) through PMU. For example, configuring PMU_HP_SLEEP_HP_PAD_HOLD_ALL can keep GPIOs in the same state as before Peripherals was powered down in HP_SLEEP.
        -   In HP_ACTIVE state, the Internal SRAMx domain can be powered down or put into Deep-sleep mode. In Deep-sleep, the memory cannot be read or written to, but data can be retained. Configure PMU_n1_HP_MEM_DSLP to enable Memory Deep-sleep mode, in which the digital power supply voltage must be higher than 0.9 V.

### 11.4.2.5 Clock Controller

The clock controller is mainly used to control high-performance system clocks and LP system clocks when the chip switches between PMU states.

High-performance system clocks include HP_ROOT_CLK and high-performance system peripherals clocks. When the chip switches between HP_ACTIVE and HP_SLEEP states, PMU can switch, power up/down, and divide the frequency of HP_ROOT_CLK, as well as power up/down high-performance system peripherals clocks.

*   **HP_ROOT_CLK can be controlled as follows:**

    -   Configure PMU_n1_SYS_CLK_SLP_SEL to 1 to indicate that when the chip enters the corresponding PMU state, the clock source is controlled by PMU.
    -   Configure PMU_n1_ICG_SYS_CLOCK_EN to 0 to disable HP_ROOT_CLK in the corresponding PMU state.
    -   Configure PMU_n1_DG_SYS_CLK_SEL to select the clock source after the chip enters the corresponding PMU state. For details, please refer to Chapter 7 Reset and Clock > Table 7.2-1.

*   **High-performance system peripheral clocks can be controlled as follows:**

    -   Configure PMU_n1_ICG_SLP_SEL to 1 so that the clock gating in the target state will be controlled by PMU. Configure this register to 0 so that the clock gating is controlled by PCR registers.
    -   Configure PMU_n1_DG_ICG_FUNC_EN to power up/down the function clock in the target PMU state. For detailed configuration please see Table 11.4-2.
```