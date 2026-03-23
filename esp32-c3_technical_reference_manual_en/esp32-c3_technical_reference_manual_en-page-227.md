

```markdown
| Power Mode | PMU | PD Peripherals | Digital System | Wireless Digital Circuits | CPU | FOSC_CLK | XTAL_CLK | PLL | RF Circuits |
|:-----------|:-----|:----------------|:---------------|:--------------------------|:-----|:----------|:----------|:-----|:-------------|
| Active     | ON  | ON             | ON            | ON                       | ON  | ON       | ON       | ON  | ON          |
| Modem-sleep| ON  | ON             | ON            | ON*                      | ON  | ON       | ON       | ON  | OFF         |
| Light-sleep| ON  | ON             | ON            | OFF*                     | OFF*| OFF*     | OFF      | OFF | OFF         |
| Deep-sleep | ON  | OFF            | OFF           | OFF                      | OFF | OFF      | OFF      | OFF | OFF         |

\* Configurable
```

```markdown
Note:
1. For details, please refer to Table 9.4-1.
2. For details on power consumption, please refer to the Current Consumption Characteristics in ESP32-C3 Datasheet.
3. For details on the supported wakeup sources, please refer to Section 9.4.3.
```

```markdown
## 9.4.3 Wakeup Source

The ESP32-C3 supports various wakeup sources, which could wake up the CPU in different sleep modes.

The wakeup source is determined by RTC_CNTL_WAKEUP_ENA as shown in Table 9.4-2.
```