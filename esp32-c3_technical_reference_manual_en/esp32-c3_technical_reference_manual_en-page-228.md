

```markdown
| WAKEUP_ENA | Wakeup Source⁵ | Light-sleep | Deep-sleep |
|------------|----------------|-------------|----------|
| 0x4        | GPIO¹          | Y           | Y        |
| 0x8        | RTC Timer      | Y           | Y        |
| 0x20       | Wi-Fi²         | Y           | -        |
| 0x40       | UARTO³         | Y           | -        |
| 0x80       | UART1³         | Y           | -        |
| 0x400      | Bluetooth      | Y           | -        |
| 0x1000     | XTAL32K_CLK⁴   | Y           | Y        |

```

9.4.4 Reject Sleep

ESP32-C3 implements a hardware mechanism that equips the chip with the ability to reject to sleep, which prevents the chip from going to sleep unexpectedly when some peripherals are still working but not detected by the CPU, thus guaranteeing the proper functioning of the peripherals.

All the wakeup sources specified in Table 9.4-2 (except UART) can also be configured as the causes to reject sleep.

Users can configure the reject to sleep option via the following registers.
*   Configure the `RTC_CNTL_SLEEP_REJECT_ENA` field to enable or disable the option to reject to sleep:
    *   Set `RTC_CNTL_LIGHT_SLP_REJECT_EN` to enable reject-to-light-sleep.
    *   Set `RTC_CNTL_DEEP_SLP_REJECT_EN` to enable reject-to-deep-sleep.
*   Read `RTC_CNTL_SLP_REJECT_CAUSE_REG` to check the reason for rejecting to sleep.

9.5 Retention DMA

ESP32-C3 can power off the CPU in Light_sleep mode to further reduce the power consumption. To facilitate the CPU to wake up from light_sleep and resume execution from the previous breakpoint, ESP32-C3
```