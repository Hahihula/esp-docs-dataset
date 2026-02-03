**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Body Text:**
through an IIR filter (moving average). touch_smooth_data is less prone to noise spikes or outlier samples, thus is the value used for hardware touch detection. The IIR filter that generates touch_smooth_data is configured via RTC_CNTL_TOUCH_SMOOTH_LVL (see Table 39.2-2).

**Subheading:**
benchmark

**Body Text:**
is also generated from touch_raw_data values through an IIR filter. However, the moving average window for benchmark is much wider. Thus, benchmark value is intended to represent the stable reading of a touch pin without the effect from a touch action. The IIR filter that generates benchmark is configured via RTC_CNTL_TOUCH_FILTER_MODE (see Table 39.2-3).

**Table Title:**
Table 39.2-2. Smooth Algorithm

| TYPE       | FORMULA                                    |
|------------|---------------------------------------------|
| -          | touch_raw_data                             |
| IIR 1/2   | 1/2 touch_raw_data + 1/2 touch_smooth_data |
| IIR 1/4   | 1/4 touch_raw_data + 3/4 touch_smooth_data |
| IIR 1/8   | 1/8 touch_raw_data + 7/8 touch_smooth_data |

**Table Title:**
Table 39.2-3. Benchmark Algorithm

| TYPE       | FORMULA                                    |
|------------|---------------------------------------------|
| IIR 1/2    | 1/2 touch_raw_data + 1/2 benchmark         |
| IIR 1/4    | 1/4 touch_raw_data + 3/4 benchmark         |
| IIR 1/8    | 1/8 touch_raw_data + 7/8 benchmark         |
| IIR 1/16   | 1/16 touch_raw_data + 15/16 benchmark      |
| IIR 1/32   | 1/32 touch_raw_data + 31/32 benchmark      |
| IIR 1/64   | 1/64 touch_raw_data + 63/64 benchmark      |
| IIR 1/128  | 1/128 touch_raw_data + 127/128 benchmark   |
| JITTER     | touch_raw_data +/- RTC_CNTL_TOUCH_JITTER STEP |

**Subheading:**
39.2.7.2 Hardware Touch Detection

**Body Text:**
Hardware touch detection can detect the conditions of touch or release, and trigger an interrupt. This removes the need to specify a software algorithm for touch detection and constantly poll for samples.

Hardware touch detection requires a finger_threshold and active_noise_threshold to be defined. When touch_smooth_data exceeds or falls short of these values the finger_threshold plus or minus hysteresis, a touch interrupt will be triggered. Both finger_threshold and active_noise_threshold are defined as offsets with respect to benchmark rather than an absolute threshold. This prevents the detection of false touches due to a gradual drift of touch_raw_data (which can be caused by various environmental factors such as temperature, power supply, or noise).

- **finger_threshold** is configured via SENS_TOUCH_OUT_THn.
- active_noise_threshold is configured via RTC_CNTL TOUCH_NOISEThRES, see Table 39.2-4.
- hysteresis is configured via RTC_CNTL TOUCH_CONFIG3, see Table 39.2-5.

**Footer:**
Espressif Systems
1462
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)