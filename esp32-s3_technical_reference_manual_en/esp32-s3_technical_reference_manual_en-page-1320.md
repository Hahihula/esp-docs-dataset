**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**Section Header:**
Register 35.1. LEDC_CHn_CONF0_REG (n : 0-7) (0x0000+0x14*n)

**Continuation Note:**
Continued from the previous page...

**Subsection Title and Description with Details:**

*LEDC_OVF_NUM_CHn*
This register is used to configure the maximum times of overflow minus
1. The LEDC_OVF_CNT_CHn_INT interrupt will be triggered when channel n overflows for (LEDC_OVF_NUM_CHn + 1) times.
- **(R/W)**

*LEDC_OVF_CNT_EN_CHn*
This bit is used to count the number of times when the timer selected by
channel n overflows. (R/W)

*LEDC_OVF_CNT_RESET_CHn*
Set this bit to reset the timer-overflow counter of channel n.
- **(WO)**

*LEDC_OVF_CNT_RESET_STChn*
This is the status bit of LEDC_OVF_CNT_RESET_CHn
- **(RO)**

**Subsection Title:**
Register 35.2. LEDC_CHn_CONF1_REG (n : 0-7) (0x000C+0x14*n)

**Table Description with Details and Values for Each Column from Left to Right, Top to Bottom:**

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| O  |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
| 1  |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |

**Subsection Title:**
LEDC_DUTY_SCALE_CHn
This register is used to configure the changing step scale of duty on channel n.
- **(R/W)**

**Subsection Title:**
LEDC_DUTY_CYCLE_CHn
The duty will change every LEDC_DUTY_CYCLE_CHn on channel n. (R/W)

**Subsection Title:**
LEDC_DUTY_NUM_CHn
This register is used to control the number of times the duty cycle will be changed.
- **(R/W)**

**Subsection Title:**
LEDC_DUTY_INC_CHn
This register is used to increase or decrease the duty of output signal on channel n. 1: Increase; 0: Decrease (R/W)

**Subsection Title:**
LEDC_DUTY_START_CHn
Configures whether or not to enable duty cycle fading.
- **(R/W)**
| 0 | Disable |
|----|---------|
| 1 | Enable |

**Footer Information:**

Espressif Systems  
Page Number and Document Version:
1320 ESP32-S3 TRM (Version 1.7)

**Link for Feedback or Documentation Submission:** 
Submit Documentation Feedback