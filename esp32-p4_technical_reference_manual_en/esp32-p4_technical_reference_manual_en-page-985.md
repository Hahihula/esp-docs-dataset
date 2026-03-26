

```markdown
| Bit in PMU_WAKEUP_ENA/PMU_LP_CPU_WAKEUP_EN | Wake-up Sources             | Source Power Domains |
|---------------------------------------------|------------------------------|-----------------------|
| 0                                           | HP_SDIO                      | PD_HP_CNNT           |
| 1                                           | Software wakeup              | PD_LP_PERI           |
| 2                                           | HP GPIO                      | PD_TOP               |
| 3                                           | HP USB                       | PD_HP_CNNT           |
| 4                                           | HP UART4                     | PD_TOP               |
| 5                                           | HP UART3                     | PD_TOP               |
| 6                                           | HP UART2                     | PD_TOP               |
| 7                                           | HP UART1                     | PD_TOP               |
| 8                                           | HP UART0                     | PD_TOP               |
| 9                                           | LP GPIO                      | PD_LP_PERI           |
| 10                                          | LP UART                      | PD_LP_PERI           |
| 11                                          | LP TOUCH                     | PD_LP_PERI           |
| 12                                          | EXT IO                       | PD_LP_PERI           |
| 13                                          | RTC_TIMER_TARO               | PD_AON               |
| 14                                          | BROWN OUT                    | PD_AON               |
| 15                                          | VBAT_UNDERTVOLAGE            | PD_AON               |
| 16                                          | LP CORE EXCEPTION            | PD_LP_PERI           |
| 17                                          | ETM                          | PD_TOP               |
| 18                                          | RTC_TIMER_TAR1               | PD_AON               |
| 19                                          | LP I2S                       | PD_LP_PERI           |
| 20                                          | GMAC PMT                     | PD_HP_CNNT           |
| 21                                          | GMAC LPI                     | PD_HP_CNNT           |
| 22                                          | LP CPU                       | PD_AON               |
| 23                                          | HP CPU                       | PD_TOP               |

```

ESP32-P4 provides a hardware mechanism that can reject sleep, meaning if some peripherals are in an uninterruptible working state and the HP CPU tries to sleep, the peripherals will send a wake-up signal to prevent the HP CPU from sleeping, thus ensuring the peripherals work normally.

The wake-up sources in Table 14.4-1 can all be configured as events to reject sleep. Users can configure the following registers to implement sleep rejection. The configuration values of PMU_SLEEP_REJECT_ENA and PMU_SLP_REJECT_CAUSE_REG and the corresponding wake-up sources are the same as shown in Table 14.4-1.

* Enable sleep rejection feature:
    * Set PMU_SLP_REJECT_EN to 1 to enable the sleep rejection feature.
    * Configure PMU_SLEEP_REJECT_ENA to select the sleep rejection signal source.
    * Read PMU_SLP_REJECT_CAUSE_REG for the source of sleep rejection event.

### 14.4.2.3 Analog Power Controller

The analog power controller controls the power up and down of the analog circuits (including voltage regulators, high-speed clocks, and slow-speed clocks) in the PMU states.
```