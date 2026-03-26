

```markdown
proximity mode. There is a separate set of threshold parameters for the sleeping touch sensor, which can be configured as follows:

* Configure LP_ANA_TOUCH_SLP_PAD to select a particular touch sensor as the sleeping touch sensor.
* Configure LP_ANA_TOUCH_SLP_TH0, LP_ANA_TOUCH_SLP_TH1, and LP_ANA_TOUCH_SLP_TH2 to set the touch threshold for the sleeping touch sensor at different frequency modes.
* Configure LP_ANA_TOUCH_SLP_APPROACH_EN to enable the proximity mode for the sleeping touch sensor.
* Configure LP_ANA_TOUCH_SLP_CHANNEL_CLR to clear the intermediate data for the sleeping touch sensor, such as benchmark, touch_raw_data, and the number of sampling.

Note:
The configuration for the noise_threshold, hysteresis, touch_smooth_data, and benchmark values are the same for the sleeping touch sensor in sleep mode as in the normal mode.
```

## 60.4.6 Moisture Tolerance

If there are water droplets on the touch pads and the droplets are large enough to physically bridge two more adjacent touch pads, the adjacent touch pads may be electrically coupled. Coupled touch pads can cause false touch detection due to capacitance changes caused by the coupling. If a water droplet is connected across the touch pad and ground, a large parasitic capacitance will be introduced, also leading to false detection. The moisture tolerance feature can mitigate the impact of water droplets.

To configure moisture tolerance:

* Configure LP_ANA_TOUCH_SHIELD_PAD_EN to enable moisture tolerance.
* Configure LP_ANA_TOUCH_BUFSEL to select a touch pin to be used for moisture tolerance.

Note:
The moisture tolerance feature only works at frequencies below 10 MHz. Therefore, when the frequency is higher than 10 MHz, please disable the moisture tolerance feature.

## 60.4.7 Water Rejection

If the sensor array becomes wet, i.e., the majority of the sensor pads are soaked by water, most (if not all) of the touch pads will become unusable due to the possible false touch detections. ESP32-P4 supports the water rejection feature to shut down the sensor array if it is detected to be wet.

Configure LP_ANA_TOUCH_OUT_RING to select one of the touch pins to be used for the water rejection feature.

## 60.5 Interrupts

ESP32-P4's touch sensor can generate the LP_TOUCH_INTR signal that will be sent to the Interrupt Matrix.
```