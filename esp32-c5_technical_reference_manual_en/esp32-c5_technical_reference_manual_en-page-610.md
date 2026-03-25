

```markdown
13.4.2.6 Backup Controller

ESP32-C5 has a Retention DMA module that can transfer data between memory and peripherals when the chip switches between PMU states, so that the data is backed up when the power domain is powered down and restored when the power domain is powered up again.

Data transfer is implemented in the Peripherals power domain. PMU only generates relevant control signals. It is important to note that the data transfer control registers are directional, as unlike other control registers, these control behaviors are determined by both the original PMU state and the target PMU state.

For example, the control registers for transitioning from HP_ACTIVE to HP_SLEEP and from HP_MODEM to HP_SLEEP are different. The possible PMU state switches are listed below, collectively represented by `PMUSTATE_TRANS` in the register names:

*   HP_SLEEP2ACTIVE
*   HP_SLEEP2MODEM
*   HP_MODEM2ACTIVE
*   HP_MODEM2SLEEP
*   HP_ACTIVE2SLEEP

The following introduces how PMU controls the Retention DMA:

*   Enable data transfer: Configure `PMU_PMUSTATE_TRANS_BACKUP_EN` to 1 to enable data transfer when the corresponding PMU state switch is performed.
*   Enable corresponding clocks: Before data transfer starts, configure `PMU_PMUSTATE_TRANS_BACKUP_CLK_SEL` to select the clock source of the Retention DMA, and configure `PMU_PMUSTATE_BACKUP_ICG_FUNC_EN` to enable the clock.

After the data transfer is completed, the value of `PMU_PMUSTATE_BACKUP_ICG_FUNC_EN` is determined by the configuration of `PMU_PMUSTATE_DIG_ICG_FUNC_EN` in the target PMU state.
*   Configure data transfer direction: Configure the highest bit of `PMU_PMUSTATE_TRANS_BACKUP_MODE`:

    -   1: From peripheral to memory
    -   0: From memory to peripheral
*   Select linked list pointer: Configure the lower four bits of `PMU_PMUSTATE_TRANS_BACKUP_MODE` to select the linked list pointer. The pointer is set within the linked list.

13.4.2.7 System Controller

The system controller controls some functional modules when the chip switches PMU states, to achieve stable and low-power chip performance. Specifically, the system controller supports:

*   Pausing the watchdog function: Configuring `PMU_PMUSTATE_DIG_PAUSE_WDT` to 1 disables the RTC watchdog timer (RWDT) function when the chip switches to the corresponding target PMU state. Note that if this register is configured to 0 in any sleep mode, the watchdog function is not disabled, and RWDT will reset as the CPU does not feed the watchdog.
*   Switching GPIO to sleep mode, where the configuration of the GPIO holds. Consider a GPIO pin working in low-drive mode as an input and a wake-up pin. Setting `PMU_PMUSTATE_HP_PAD_HOLD_ALL` to 1
```