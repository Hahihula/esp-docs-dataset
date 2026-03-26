

```markdown
signals. The scanning process is shown in Figure 60.4-4.

Figure 60.4-4. Touch Sensor Frequency Hopping Sequence Timing

Set LP_ANA_FREQ_SCAN_EN to 1 to enable frequency hopping, configure LP_ANA_FREQ_SCAN_CNT_LIMIT to select the maximum number of frequency mode supported, and configure the following analog parameter registers to adjust the sampling performance of the touch sensor at different frequency modes:

*   LP_ANA_TOUCH_FREQn_DBIAS (n = 0-2)
*   LP_ANA_TOUCH_FREQn_DRV_HS (n = 0-2)
*   LP_ANA_TOUCH_FREQn_DRV_LS (n = 0-2)
*   LP_ANA_TOUCH_FREQn_DRES_LPF (n = 0-2)
*   LP_ANA_TOUCH_FREQn_CAP_LPF (n = 0-2)

Upon each START signal, the Touch FSM measures consecutively for frequency mode 0, 1, and 2. A START signal triggers a maximum of three measurement operations. When the measurements are completed for all frequency modes, the START signal is de-asserted until the next measurement. Therefore, the Touch FSM performs measurements on the enabled touch sensors in sequence upon multiple START signals. A touch on the same sensor is recognized only when the number of hit frequency points is greater than or equal to LP_ANA_FREQ_SCAN_CNT_RISE.

Note:

*   When the same touch sensor is measured at different frequency modes, the wait time between measurements can be configured by LP_ANA_TOUCH_XPD_WAIT (count clock: AON_FAST_CLK).
*   After receiving the START signal from the touch timer, the touch sensor waits for a short period of time before starting measuring to ensure the stability of the sampling signal. The wait time can be configured by LP_ANA_TOUCH_XPD_WAIT (count clock: AON_FAST_CLK).
*   If a touch timer is used to generate the START signal, the scanning can be conducted without software intervention.
```