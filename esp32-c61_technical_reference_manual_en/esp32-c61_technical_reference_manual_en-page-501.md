

```markdown
| PMU_WAKEUP_ENA | Wake-up Sources | Light-sleep | Deep-sleep |
|----------------|-----------------|-------------|------------|
| 0x4            | GPIO¹           | Y           | Y          |
| 0x8            | Wi-Fi beacon    | Y           | N          |
| 0x10           | RTC Timer       | Y           | Y          |
| 0x20           | Wi-Fi²          | Y           | –          |
| 0x40           | UARTO³          | Y           | –          |
| 0x80           | UART1³          | Y           | –          |
| 0x100          | SDIO            | Y           | –          |
| 0x400          | Bluetooth       | Y           | –          |

```

```markdown
1 In Deep-sleep mode, only the LP GPIOs can work as wake-up sources.
2 To wake up the chip with Wi-Fi, the chip switches between Active, Modem-sleep, and Light-sleep modes. The RF module is woken up at predetermined intervals by timers to keep Wi-Fi connectivity and communication.
3 A wake-up is triggered when the number of RX pulses received exceeds the threshold set in UART_ACTIVE_THRESHOLD. For details, please refer to Chapter 25 UART Controller (UART).
```

## 11.4.2.3 Analog Power Controller

The analog power controller controls the power up and down of the analog circuits (including voltage regulators, high-speed clocks, and slow-speed clocks) in PMU states.

The configuration of the regulators is as follows:

* Configure (**PMU_PMUSTATE_HP_REGULATOR_XPD**) or (**PMU_PMUSTATE_LP_REGULATOR_XPD**) to enable or disable the output voltage of the HP/LP regulators in the target PMU state. Turning off the LP regulators is not recommended, as it may cause the PMU itself to power down, resulting in chip malfunction.

The configuration of the high-speed clocks (XTAL_CLK and PLL_CLK) is as follows:

* XTAL_CLK: Configure **PMU_HP_SLEEP_XPD_XTAL** to 1 to enable XTAL_CLK when the chip switches PMU state to HP_SLEEP.
```