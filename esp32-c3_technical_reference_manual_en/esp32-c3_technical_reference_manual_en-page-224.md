
```markdown
| RTC_CNTL_TIMER_XTL_OFF | 1. RTC main state machine powers down; 2. 40 MHz crystal powers up. |
|-------------------------|--------------------------------------------------------------------|
| RTC_CNTL_TIMER_SYSSTALL | CPU enters or exits the stall state. This is to ensure the SYS_TIMER is continuous in time. |
| RTC_CNTL_TIMER_SYS_RST | Resetting digital system completes.                             |
| RTC_CNTL_TIME_UPDATE    | Register `RTC_CNTL_TIME_UPDATE` is configured by CPU (i.e. users). |
```

The RTC timer updates two groups of registers upon any new trigger. The first group logs the time of the current trigger, and the other logs the previous trigger. Detailed information about these two register groups is shown below:

- Register group 0: logs the status of RTC timer at the current trigger.
    - `RTC_CNTL_TIME_HIGH0_REG`
    - `RTC_CNTL_TIME_LOW0_REG`

- Register group 1: logs the status of RTC timer at the previous trigger.
    - `RTC_CNTL_TIME_HIGH1_REG`
    - `RTC_CNTL_TIME_LOW1_REG`

On a new trigger, information on previous trigger is moved from register group 0 to register group 1 (and the original trigger logged in register group 1 is overwritten), and this new trigger is logged in register group 0. Therefore, only the last two triggers can be logged at any time.

It should be noted that any reset / sleep other than power-up reset will not stop or reset the RTC timer.

Also, the RTC timer can be used as a wakeup source. For details, see Section 9.4.3.

## 9.3.4 Voltage Regulators

ESP32-C3 has two regulators to maintain a constant power supply voltage to different power domains:

- Digital system voltage regulator for digital power domains;
- Low-power voltage regulator for RTC power domains;

**Note:**

For more detailed description about power domains, please refer to Section 9.4.1.

### 9.3.4.1 Digital System Voltage Regulator

ESP32-C3’s built-in digital system voltage regulator converts the external power supply (typically 3.3 V) to 1.1 V for digital power domains. This regulator is controlled by the `xpd_dig_reg` signal. For details, see description in 9.3-1. For the architecture of the ESP32-C3 digital system voltage regulator, see Figure 9.3-5.
```