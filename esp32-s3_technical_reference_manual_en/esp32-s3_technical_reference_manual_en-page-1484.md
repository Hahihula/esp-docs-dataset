**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Register Section Header:**
Register 39.6. RTC_CNTL_TOUCH_FILTER_CTRL_REG (0x11C)

**Binary Register Diagram Description with Labels for Each Bit Field:**
- RTC_CNTL_TOUCH_FILTER_EN
- RTC_CNTL TOUCH_FILTER_MODE
- RTC_CNTL_TOUCH_CONFIG1
- RTC_CNTL_TOUCH_CONFIG2
- RTC_CNTL_TOUCHConfig3
- RTC_CNTL_TOUCH_CONFIG4
- RTC_CNTL_TOUCHConfig5

**Field Descriptions and Values in Binary Format with Explanation for Each Field:**

1. **RTC_CNTL_TOUCH_SMOOTH_LVL**
   - Description: Smooth filter factor.
   - Options:
     0: Raw data (R/W)
     1: IIR/2
     2: IIR/4
     3: IIR/8

2. **RTC_CNTL_TOUCH_JITTER_STEP**
   - Description: Touch jitter step range, from R to W.
   - Range: 0 ~ 15 (R/W)

3. **RTC_CNTL_TOUCH_CONFIG1** 
   - Description: Internal configuration field.

4. **RTC_CNTL TOUCH_CONFIG2**
   - Description: Internal configuration field for touch filter control register.

5. **RTC_CNTL_TOUCH_NOISE_THRES**
   - Description: Active noise threshold.
   - Range (R/W): 0 ~ 6

6. **RTC_CNTL_TOUCH_CONFIG3** 
   - Description: Internal configuration field, set to enable or disable the feature based on bit values:
     - IIR/128
     - Jitter filter mode selection.

7. **RTC_CNTL TOUCH_FILTER_MODE**
   - Description: Set filter mode.
   - Options (R/W):
     0: IIR /2
     1: IIR /4
     2: IIR /8
     3: IIR /16
     4: IIR /32
     5: IIR /64
     6: IIR /128

8. **RTC_CNTL_TOUCH_FILTER_EN**
   - Description: Enable touch filter.
   - Range (R/W): On or Off.

**Footer Information:** 
Espressif Systems, ESP32-S3 TRM (Version 1.7), Page number is not specified but the document ends with "Submit Documentation Feedback".