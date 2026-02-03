**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Link:**
GoBack

**Subtitle:**
10.4.2 RTC States

**Body Text:**
ESP32-S3 has three main RTC states: Active, Monitor, and Sleep. The transition process among these states can be seen in Figure 10.4-1.

**Figure Caption:**
Figure 10.4-1. RTC States
```
Active
|
Monitor -- ULT done or touch done --
Sleep   |
|
ULP timer or touch timer
```

**Additional Text:**
Under different RTC states, different power domains are powered up or down by default, but can also be force-powered-up (FPU) or force-powered-down (FPD) individually based on actual requirements. For details, please refer to Table 10.4-1.

**Footer Information:**
Espressif Systems
577 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback