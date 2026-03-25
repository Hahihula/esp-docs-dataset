

```markdown
| PMU_WAKEUP_ENA | Wake-up Sources     | Light-sleep0 | Deep-sleep |
|----------------|---------------------|--------------|------------|
| 0x2            | EXT                 | Y            | Y          |
| 0x4            | GPIO¹               | Y            | –          |
| 0x10           | RTC Timer           | Y            | Y          |
| 0x40           | UART0²              | Y            | –          |
| 0x80           | UART1²              | Y            | –          |
| 0x400          | Bluetooth           | Y            | –          |
| 0x2000         | Brown-out           | Y            | –          |
| 0x8000         | vbat_detect         | Y            | –          |

¹ In Deep-sleep mode, only the LP GPIOs can work as wake-up sources.
² A wake-up is triggered when the number of RX pulses received exceeds the threshold set in UART_ACTIVE_THRESHOLD. For details, please refer to Chapter 28 UART Controller (UART).
```

ESP32-H2 provides a hardware mechanism that can reject sleep, meaning if some peripherals are in an uninterruptible working state and the CPU tries to sleep, the peripherals will send a wake-up signal to prevent the CPU from sleeping, thus ensuring the peripherals work normally.

The wake-up sources in Table 11.4-1 can all be configured as events to reject sleep. Users can configure the following registers to implement sleep rejection. The configuration values of PMU_SLEEP_REJECT_ENA and PMU_SLP_REJECT_CAUSE_REG and the corresponding wake-up sources are the same as shown in Table 11.4-1.

*   Enable sleep rejection feature:
    *   Set PMU_SLP_REJECT_EN to 1 to enable the sleep rejection feature.
    *   Configure PMU_SLEEP_REJECT_ENA to enable the sleep rejection signal source.
*   Read PMU_SLP_REJECT_CAUSE_REG for the source of sleep rejection event.

### 11.4.2.3 Analog Power Controller

The analog power controller controls the power up and down of the analog circuits (including voltage regulators, high-speed clocks, and slow-speed clocks) in PMU states.

The configuration of the regulators is as follows:

*   Configure PMU_n1_HP_REGULATOR_XPD or PMU_n1_LP_REGULATOR_XPD to enable or disable the output voltage of the HP/LP sys regulator in the target PMU state. Turning off the LP sys regulator is not recommended, as it may cause the PMU itself to power down, resulting in chip malfunction.

The configuration of the high-speed clocks (XTAL_CLK and PLL_CLK) is as follows:
```