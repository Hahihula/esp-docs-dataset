

```markdown
- Enable corresponding clocks: Before data transfer starts, configure PMU_n2_BACKUP_CLK_SEL to select the clock source of the Retention DMA, and configure PMU_n1_BACKUP_ICG_FUNC_EN to enable the clock.

After the data transfer is completed, the value of PMU_n1_BACKUP_ICG_FUNC_EN is determined by the configuration of PMU_n1_DIG_ICG_FUNC_EN in the target PMU state.

- Configure data transfer direction: Configure the highest bit of PMU_n2_BACKUP_MODE:
  - 1: From peripheral to memory
  - 0: From memory to peripheral

- Select linked list pointer: Configure the lower two bits of PMU_n2_BACKUP_MODE to select the linked list pointer, specifically:
  - 0: PAU_LINK_ADDR_0
  - 1: PAU_LINK_ADDR_1
  - 2: PAU_LINK_ADDR_2
  - 3: PAU_LINK_ADDR_3

### 12.4.2.7 System Controller

The system controller controls some functional modules when the chip switches PMU states, to achieve stable and low-power chip performance. Specifically, the system controller supports:

- Pausing the watchdog function: Configuring PMU_n1_DIG_PAUSE_WDT to 1 can disable the RTC watchdog timer (RWDT) function when the chip switches to the corresponding target PMU state. Note that if this register is configured to 0 in any sleep mode, the watchdog function is not disabled, and RWDT will reset as the CPU does not feed the watchdog.

- Switching GPIO to sleep mode, where the configuration of the GPIO holds. Consider a GPIO pin working in low-drive mode as an input and a wake-up pin. Setting PMU_n1_HP_PAD_HOLD_ALL to 1 can latch the current configuration of the GPIO pin as the sleep configuration when the chip transitions to the corresponding PMU state. For more information about GPIO's hold function, please refer to Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX) > Section 7.9.

- Disabling UART wake-up function: Configuring PMU_n1_UART_WAKEUP_EN to 0 can disable the four UART wake-up modes in the corresponding PMU state. For more information on UART wake-up modes, please refer to Chapter 27 UART Controller (UART, LP_UART, UHCI).

- Pausing CPU: Setting PMU_n1_DIG_CPU_STALL to 1 can suspend the CPU in the corresponding PMU state.

### 12.4.3 RTC Timer

ESP32-C6's low-power management system features an RTC timer. The 48-bit RTC timer is a real-time counter that logs time when certain events occur, working at RTC_SLOW_CLK. For the trigger conditions for the RTC timers, see Table 12.4-4.

**Table 12.4-4. Trigger Conditions for the RTC Timer**
```