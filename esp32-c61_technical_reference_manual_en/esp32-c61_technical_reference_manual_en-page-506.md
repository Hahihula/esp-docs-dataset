
```markdown
- 3: PAU_LINK_ADDR_3


11.4.2.7 System Controller

The system controller controls some functional modules when the chip switches PMU states, to achieve stable and low-power chip performance. Specifically, the system controller supports:

* Pausing the watchdog function: Configuring `PMU_PMUSTATE_DIG_PAUSE_WDT` to 1 can disable the RTC watchdog timer (RWDT) function when the chip switches to the corresponding target PMU state. Note that if this register is configured to 0 in any sleep mode, the watchdog function is not disabled, and RWDT will reset as the CPU does not feed the watchdog.

* Switching GPIO to sleep mode, where the configuration of the GPIO holds. Consider a GPIO pin working in low-drive mode as an input and a wake-up pin. Setting `PMU_PMUSTATE_HP_PAD_HOLD_ALL` to 1 can latch the current configuration of the GPIO pin as the sleep configuration when the chip transitions to the corresponding PMU state. For more information about GPIO's hold function, please refer to Chapter 6 GPIO Matrix and IO MUX > Section 6.9.

* Disabling UART wake-up function: Configuring `PMU_PMUSTATE_UART_WAKEUP_EN` to 0 can disable the four UART wake-up modes in the corresponding PMU state. For more information on UART wake-up modes, please refer to Chapter 25 UART Controller (UART).

* Pausing CPU: Setting `PMU_PMUSTATE_DIG_CPU_STALL` to 1 can suspend the CPU in the corresponding PMU state.


11.4.3 RTC Timer

ESP32-C61's low-power management system features an RTC timer. The 48-bit RTC timer is a real-time counter that logs time when certain events occur, working at LP_DYN_FAST_CLK. For the trigger conditions for the RTC timer, see Table 11.4-2.

Table 11.4-2. Trigger Conditions for the RTC Timer

| Triggering Conditions | Description |
|-----------------------|-------------|
| `RTC_TIMER_MAIN_TIMER_XTAL_OFF` | Triggered when PMU powers up or down the 40 MHz crystal. |
| `RTC_TIMER_MAIN_TIMER_SYS_STALL` | Triggered when the CPU enters or exits the stall state. This is to ensure the system timer is continuous in time. |
| `RTC_TIMER_MAIN_TIMER_SYS_RST` | Triggered upon system reset. |
| `RTC_TIMER_MAIN_TIMER_UPDATE` | Triggered when `RTC_TIMER_MAIN_TIMER_UPDATE` is configured by the CPU (e.g., users). |

The RTC timer updates two groups of registers upon any new trigger.

* Register group 0 records the count value of the RTC timer under the current trigger, with the counting unit being LP_DYN_SLOW_CLK.
    - `RTC_TIMER_MAIN_TIMER_TAR_HIGHO`
    - `RTC_TIMER_MAIN_TIMER_TAR_LOW0`
```