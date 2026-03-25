

```markdown
Note:
In the following text, all such registers will be collectively referred to as PMU_PMUSTATE_PD_POWERDOMAIN_PD_EN.
where PMUSTATE represents the four PMU states.

Once the configuration is done, PMU uses various controllers to make these configurations effective, as described in the sections below.

13.4.2.2 Sleep/Wake-up Controller

The sleep/wake-up controller initiates sleep and wake-up requests to the PMU main state machine. ESP32-C5 supports multiple wake sources to wake the CPU from different power modes. Table 13.4-1 lists all the wake-up sources.

Table 13.4-1. Wake-up Sources

| PMU_WAKEUP_ENA | Wake-up Sources                | Light-sleep | Deep-sleep |
|----------------|--------------------------------|-------------|------------|
| 0x2            | EXT_IO¹                        | Y           | Y          |
| 0x4            | GPIO¹                          | Y           | Y          |
| 0x8            | Wi-Fi beacon                   | Y           | -          |
| 0x10           | RTC Timer                      | Y           | Y          |
| 0x20           | Wi-Fi²                         | Y           | –          |
| 0x40           | UARTO³                         |             | –          |
| 0x80           | UART1³                         |             | –          |
| 0x100          | SDIO slave controller⁴         |             | –          |
| 0x400          | Bluetooth                      |             | –          |
| 0x800          | LP CPU                         |             | Y          |

¹ In Deep-sleep mode, only the LP GPIOs can work as wake-up sources.
² To wake up the chip with Wi-Fi, the chip switches between Active, Modem-sleep, and Light-sleep modes. The RF module is woken up at predetermined intervals to keep Wi-Fi connectivity and communication.
³ A wake-up is triggered when the number of RX pulses received exceeds the threshold set in UART_ACTIVE_THRESHOLD. For details, please refer to Chapter 32 UART Controller (UART).
⁴ When the SDIO lave controller receives CMD52 CMD53, it triggers wake-up. This wake-up feature requires the sleep voltage to be higher than 0.9 V, and the voltage configuration varies across different chips due to manufacturing differences.

ESP32-C5 provides a hardware mechanism that can reject sleep, meaning if some peripherals are in an uninterruptible working state and the CPU tries to sleep, the peripherals will send a wake-up signal to prevent the CPU from sleeping, thus ensuring the peripherals work normally.

The wake-up sources in Table 13.4-1 can all be configured as events to reject sleep. Users can configure the following registers to implement sleep rejection. The configuration values of PMU_SLEEP_REJECT_ENA and PMU_SLP_REJECT_CAUSE_REG and the corresponding wake-up sources are the same as shown in Table 13.4-1.
```