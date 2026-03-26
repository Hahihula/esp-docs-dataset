

```markdown
Chapter 60 Touch Sensor (TOUCH)

GoBack

60.4.2.2 Trigger Source of Measurement

The Touch FSM initiates a measurement by sending a START signal. The START signal can either be triggered by software, or by a dedicated hardware timer known as the "touch timer". The use of a touch timer allows periodic measurements to be taken without software intervention.

The touch timer is clocked by LP_DYN_SLOW_CLK and should be configured with a period in number of LP_DYN_SLOW_CLK cycles. The START signal is generated when the touch timer expires. The touch timer is reset when the measurement completes and restarts counting until the next expiration.

- To trigger the START signal by software:
  - Set `LP_ANA_TOUCH_START_FORCE` to 1 to trigger the START signal by software.
  - Software sets `LP_ANA_TOUCH_START_EN` to 1 and generates the START signal to initiate a measurement.

- To trigger the START signal by the touch timer:
  - Clear `LP_ANA_TOUCH_START_FORCE`.
  - Configure the wait time before the timer sends the START signal (unit: LP_DYN_SLOW_CLK cycle) via `PMU_TOUCH_WAIT_CYCLES`.
  - Configure the wait time after the timer receives the DONE signal upon completion of the touch sensor sampling (unit: LP_DYN_SLOW_CLK cycle) via `PMU_TOUCH_SLEEP_CYCLES`.
  - Set `PMU_TOUCH_SLEEP_TIMER_EN` to 1 to enable the touch timer.

- To force exit the current measurement cycle of the touch timer by software, there are two approaches:

  1. Generate the end signal of the touch sensor to exit the current measurement cycle of the touch timer.
     - Set `LP_ANA_TOUCH_DONE_FORCE` to 1 to select the DONE signal to be triggered by software.
     - Software sets `LP_ANA_TOUCH_DONE_EN` to 1 to generate the DONE signal to end a measurement.

  2. Use the software to directly force the touch timer to exit the current measurement cycle.
     - Set `PMU_TOUCH_FORCE_DONE` to generate the DONE signal and force the touch timer to exit the current measurement cycle.

Note:
The touch timer waits for a period of time before generating the START signal and after receiving the DONE signal, so the interval between two consecutive measurements is (`PMU_TOUCH_WAIT_CYCLES + PMU_TOUCH_SLEEP_CYCLES`) and the timing clock is LP_DYN_SLOW_CLK.

60.4.2.3 Scan Mode

Scan mode involves the Touch FSM taking measurements of multiple touch sensors in sequential order. On every START signal, a new touch sensor is selected for measurement, thus allowing multiple touch pins to be monitored. The scan process is illustrated in Figure 60.4-3.
```