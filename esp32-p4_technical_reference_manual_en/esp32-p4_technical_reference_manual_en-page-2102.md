

```markdown
Note:

It is recommended to let the VAD module learn noise parameters during the initialization. However, the VAD module will also continuously learn and update noise parameters during normal operation. Therefore, in scenarios where the false positive rate during initial frames is not a concern, the number of initial frames can be reduced, allowing the VAD module to enter the normal operation more quickly.

Energy Threshold

The VAD module sets an energy threshold before the voice activity detection. Setting the threshold can filter out low-energy voice activities (e.g., distant voices) from triggering a wake-up. Appropriate energy threshold setting can effectively reduce false positives and conserve power.

It defines the energy value of a speech frame as the mean square of one-frame data. The VAD module calculates the sum of squares of one-frame data in real-time. If this sum is less than the energy threshold multiplied by 256, subsequent calculations will not be performed. Users can configure the energy threshold via LP_I2S_PARAM_MIN_ENERGY.

Band Energy Check

The band energy check assesses the proportion of band energy within the overall frequency spectrum.
Enabling the band energy check in varying environments can help reduce false positives; however, it may also reduce true positives. Users should determine whether to enable or disable the band energy check based on the environment.

Users can enable or disable the band energy check via LP_I2S_PARAM_SKIP_BAND_ENERGY.

- 0: Enable band energy check
- 1: Disable band energy check

Voice Activity Detection

The VAD module has two voice activity status: voice activity status and non-voice activity status, managed by voice frame counter speech_count and non-voice frame counter silent_count. These counters control transitions between the status as follows:

• Non-voice activity status:
  - When voice activities are detected in the current frame, the count value of speech_count increases by 1.
  - When voice activities are not detected in the current frame, the count value of speech_count decreases by 1 (down to a minimum of 0).
  - If the count value of speech_count is greater than LP_I2S_PARAM_HANGOVER_SPEECH, the VAD module enters the voice activity status and resets silent_count to 0.
  - Under the non-voice activity status, the VAD module continuously learns and updates noise information.

• Voice activity status:
  - When voice activities are detected in the current frame, the count value of speech_count increases by 1, and the count value of silent_count decreases by 1 (down to a minimum of 0).
```