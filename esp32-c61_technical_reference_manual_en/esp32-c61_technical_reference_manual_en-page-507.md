

```markdown
- Register group 1 records the count value of the RTC timer under the previous trigger, with the counting unit being LP_DYN_SLOW_CLK.
  - RTC_TIMER_MAIN_TIMER_TAR_HIGH1
  - RTC_TIMER_MAIN_TIMER_TAR_LOW1

Each time there is a new trigger, the record from the previous trigger will be moved from register group 0 to register group 1 (the record in register group 1 will be overwritten), and the record of the current trigger will be stored in register group 0. Therefore, the RTC timer can record up to two trigger values simultaneously.

It is worth noting that any reset or sleep state other than the chip’s power-up reset will not stop or reset the RTC timer, which is in the LPSYS power domain. Additionally, the RTC timer can also be used as a wake-up source (see Table 11.4-1).

## 11.5 Power Modes

ESP32-C61 has four configurable PMU states. Based on the four PMU states, five power modes have been defined for the most commonly seen application scenarios. For the details, please see Table 11.5-1.

Table 11.5-1. Preset Power Modes

| Power Modes | LPSYS | LPSYS_OFF | ROM + Peripherals | Modem | CPU | RC_FAST_CLK | XTAL_CLK | PLL | RF circuit |
|-------------|-------|-----------|-------------------|-------|-----|-------------|----------|-----|------------|
| Active      | ON    | ON        | ON                | ON    | ON  | ON          | ON       | ON  | ON         |
| Modem-sleep | ON    | ON        | ON                | ON    | OFF | ON          | ON       |     | OFF        |
| Light-sleep0| ON    | ON        | ON                | ON/OFF|OFF | ON          | ON/OFF   |     | ON/OFF     |
| Light-sleep1| ON    | ON/OFF    | ON/OFF            | ON/OFF|OFF | ON/OFF      | ON/OFF   |     | ON/OFF     |
| Deep-sleep  | ON    | OFF       | OFF               | OFF   | OFF | OFF         | OFF      |     | OFF        |

Note:
1. [ESP32-C61 Datasheet](#) > Section Current Consumption.
2. For supported wake-up sources, please refer to Table 11.4-1.

## 11.6 Event Task Matrix Feature

The low-power management system on ESP32-C61 supports the Event Task Matrix (ETM) function, which allows the low-power management system’s ETM tasks to be triggered by any peripherals’ ETM events, or the low-power management system’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to the low-power management system. For more information, please refer to Chapter 10 Event Task Matrix (ETM).

The low-power management system can receive the following ETM tasks:
```