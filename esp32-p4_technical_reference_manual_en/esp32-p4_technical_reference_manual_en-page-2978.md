

```markdown
Figure 60.4-3. Timing Diagram of Scan Mode

To enable the scan mode, specify the bit map of the enabled touch pins in `LP_ANA_TOUCH_SCAN_PAD_MAP`. The Touch FSM will select one touch pin from the bit map of the enabled touch pins in turn to measure per START signal, i.e., only one measurement is conducted per START signal. As multiple START signals are generated, the Touch FSM will cycle through the enabled touch pins in sequential order.

When measuring for different touch sensors, the sleep interval between two measurements is `PMU_TOUCH_WAIT_CYCLES + PMU_TOUCH_SLEEP_CYCLES` with the clock cycle of `LP_DYN_SLOW_CLK`.

Note:
* After the touch sensor receives the START signal from the touch timer, it waits a short period before starting the measurement to ensure the stability of the sampling signal. The wait time is configured by `LP_ANA_TOUCH_XPD_WAIT`. The timing clock is `AON_FAST_CLK`.
* If the touch timer is used to generate the START signal, the scanning can be conducted without software intervention.

60.4.2.4 Frequency Hopping

When frequency hopping is enabled, the Touch FSM can measure the touch sensor at different frequency modes. Up to three frequency modes are supported, each corresponding to a set of configuration parameters. When a START signal is generated, the measurement will be carried out for each frequency mode sequentially, and the DONE signal will be generated when the measurements are completed for all frequency modes. Frequency hopping can be enabled together with the scan mode. In such case, users can monitor the touch condition of multiple touch sensors under different frequency modes by generating multiple START
```