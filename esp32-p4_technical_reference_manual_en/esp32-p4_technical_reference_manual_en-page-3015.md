

```markdown
- TMPSNSR_EVT_OVER_LIMIT: Generated when the temperature is beyond the threshold.

In practical applications, the temperature sensor’s ETM events can trigger its own ETM tasks. For example, the TMPSNSR_EVT_OVER_LIMIT event can trigger the TMPSNSR_TASK_STOP_SAMPLE task.
```

## 61.6 Interrupts

ESP32-P4's Temperature Sensor can generate the following interrupt signal that will be sent to the [Interrupt Matrix](#).

- LP_TSENS_INTR

There is one internal interrupt source from the Temperature Sensor that can generate the above interrupt signal:

- TSENS_COCPU_TSENS_WAKE_INT: Triggered when the temperature sample value exceeds the threshold.

**Note:**

For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 [Interrupt Matrix](#) > Section 12.2 Interrupt Terminology in ESP32-P4.

Each interrupt source can be configured by a common set of registers that are described in Section [Interrupt Configuration Registers](#). The specific registers can be found in Section [61.8 Register Summary](#).

## 61.7 Programming Procedure

The temperature sensor can be started by software as follows:

1. Set `TSENS_POWER_UP` to power up the temperature sensor.
2. Set `LPPERI_CK_EN_LP_TSENS` to enable the temperature sensor clock.
3. Wait for `TSENS_XPD_WAIT` clock cycles till the temperature sensor releases from reset and starts measuring the temperature.
4. Wait for 100 µs (so that the output value gradually approaches the actual temperature) and then read the data from `TSENS_OUT`.

To enable hardware-triggered automatic temperature monitoring, add the following programming steps before powering up the sensor:

1. Configure `TSENS_SAMPLE_RATE` to set sampling rate.
2. Configure `TSENS_WAKEUP_MODE` to select wake-up mode for temperature monitoring.
3. Configure `TSENS_WAKEUP_TH_HIGH/LOW` to set the high and low temperature monitoring thresholds.
4. Set `TSENS_WAKEUP_EN` to start temperature monitoring.
5. Set `TSENS_SAMPLE_EN` to enable automatic temperature monitoring.

In automatic temperature monitoring mode, the output value will not be saved. Nevertheless, users can get the value at any moment by accessing `TSENS_OUT`.
```