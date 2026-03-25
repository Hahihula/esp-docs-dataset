

```markdown
5. Wait for 100 µs (so that the output value gradually approaches the actual temperature) and then read the data from `APB_SARADC_TSENS_OUT`.

To enable hardware-triggered automatic temperature monitoring, add the following programming steps before powering up the sensor:

1. Configure `APB_SARADC_TSENS_SAMPLE_RATE` to set sampling rate.
2. Configure `APB_SARADC_WAKEUP_MODE` to select an automatic temperature monitoring mode.
3. Configure `APB_SARADC_WAKEUP_TH_HIGH/LOW` to set the high and low temperature monitoring thresholds.
4. Set `APB_SARADC_WAKEUP_EN` to start temperature monitoring.
5. Set `APB_SARADC_TSENS_SAMPLE_EN` to enable automatic temperature monitoring.

In automatic temperature monitoring mode, the output value will not be stored. However, users can get the value anytime from `APB_SARADC_TSENS_OUT`.

## 45.6 Interrupts

ESP32-C5’s Temperature Sensor can generate the following interrupt signal that will be sent to the **Interrupt Matrix**.

*   LP_TSENS_INTR

There is one internal interrupt source from the Temperature Sensor that can generate the above interrupt signal:

*   `APB_SARADC_TSENS_INT`: Triggered when the temperature sample value exceeds the threshold.

**Note:**

For definitions of *interrupt*, *interrupt signal*, *interrupt source*, and their correlations, please refer to Chapter 11 **Interrupt Matrix > Section 11.2 Terminology**.

Each interrupt source can be configured by a common set of registers that are described in Section **Interrupt Configuration Registers**. The specific registers can be found in Section **45.8 Register Summary**.

## 45.7 Event Task Matrix Feature

The temperature sensor on ESP32-C5 supports the Event Task Matrix (ETM) function, which allows the temperature sensor’s ETM tasks to be triggered by any peripherals’ ETM events, or temperature sensor’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to the temperature sensor. For more information, please refer to Chapter 12 **Event Task Matrix (ETM)**.

The temperature sensor can receive the following ETM tasks:

*   `TMPNSR_TASK_START_SAMPLE`: The temperature sensor starts sampling when this task is triggered.
*   `TMPNSR_TASK_STOP_SAMPLE`: The temperature sensor stops sampling when this task is triggered.

The temperature sensor can generate the following ETM events:
```