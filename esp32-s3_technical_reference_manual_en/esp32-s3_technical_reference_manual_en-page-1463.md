**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Tables:**

- **Table 39.2-4. Noise Algorithm**
  - RTC_CNTL_TOUCH_NOISE_THRES | FORMULA
    - 0 | 4/8 finger threshold
    - 1 | 3/8 finger threshold
    - 2 | 2/8 finger threshold
    - 3 | 1/8 finger threshold

- **Table 39.2-5. Hysteresis Algorithm**
  - RTC_CNTL_TOUCH_CONFIG3 | FORMULA
    - 0 | 1/8 finger threshold
    - 1 | 3/32 finger threshold
    - 2 | 1/32 finger threshold

**Subsections:**

- **39.2.8 Noise Detection**
  - Touch sensor O is not connected to any GPIO (i.e., not connected to an external touch panel). Therefore, any fluctuations in the capacitance measured by touch sensor O will represent the internal noise. The Noise Detection feature allows touch sensor O to be used as a noise reference. When touch sensor N (1 ~ 14) takes a measurement, touch sensor O will simultaneously measure as well. The sampled value of touch sensor O can be subtracted from the sampled value of touch sensor N automatically to decrease the effect of noise.

    - **The following points describe the Noise Detection feature:**
      - Configure the drive strength of touch sensor 0 by adjusting its reference capacitance via RTC_CNTL_TOUCH_REFC.
      - Set RTC_CNTL TOUCH_DENOISE_EN to 1. Once set, when another touch sensor N starts a measurement, touch sensor O will start a measurement simultaneously.

      The final sampled value will be DATA(TOUCH[N]) - DATA(TOUCHO). DATA(OUCH[N]) is the value sampled by touch sensor N, and DATA(TOUCHO) are the least significant bits of the value sampled by touch sensor 0. DATA(TOUCHO) can be 12/10/8/4 bits of the sampled value of touch sensor O, depending on the configuration of RTC_CNTL TOUCH_DENOISE_RES.

- **39.2.9 Proximity Mode**
  - When an object (e.g., a finger) is placed proximate (but not touching) a touch pin, a small change in capacitance will occur on the touch pin (much smaller compared to a physical touch). Proximity mode allows for the detection of these small changes.

    - The maximum detection distance (d) is 16 cm with a sensing area of 20 cm² (S), where d is positively correlated with S as shown in Figure **39.2-6**.
    - Up to three touch pins can be configured to operate in proximity mode.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback