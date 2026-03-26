

```markdown
Chapter 41 Voice Activity Detection (VAD) GoBack


Figure 41.3-1. ESP32-P4 VAD Architecture



The VAD module reads 8 kHz, 16-bit wide audio data from LP I2S memory. It processes the data through three stages: energy detection, FFT, and LTSD. Then the module detects the voice activity status and sends the VAD status signal to the LP I2S module, which is used to generate the corresponding interrupt and wake-up signal.



41.4 Functional Description

The ESP32-P4’s VAD module offers flexible and configurable functionality. Users can adjust algorithm parameters and wake-up sources to meet their specific needs.



41.4.1 Algorithm Parameter Configuration



Number of Initial Frames

When the VAD module starts running, it first enters an initialization phase before normal operation. During this phase, it automatically learns noise parameters. The duration of the initialization phase depends on the number of initial frames configured by the user. Proper setting of initial frames can effectively suppress noise and significantly reduce false positives. However, if the initialization phase is extended over too many frames, voice activity within these frames may be missed. Therefore, please configure an appropriate number of initial frames based on actual conditions.

It is recommended to place the device in the target environment noise during the initialization, and set the number of initial frames to 100-200 frames.

Users can configure the number of initial frames via LP_I2S_PARAM_INIT_FRAME_NUM.
```