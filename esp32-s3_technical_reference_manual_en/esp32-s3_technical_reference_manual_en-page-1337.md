**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Body Text:**
period value - 1], and when the counting direction is decreasing, the timer range is [period value, 1]. That is, in this mode, when synchronizing the timer to 0, decreasing counting direction will be illegal, namely,

`MCPWM_TIMERn_PHASE_DIRECTION` cannot be set to 1. Similarly, when synchronizing the timer to period value, increasing counting direction will be illegal, namely, `MCPWM_TIMERn_PHASE_DIRECTION` cannot be set to 0. Therefore, when the timer is synchronized to 0, the counting direction can only be increasing, and `MCPWM_TIMERn_PHASE_DIRECTION` will be 0. When the timer is synchronized to the period value, the counting direction can only be decreasing, and `MCPWM_TIMERn_PHASE_DIRECTION` will be 1.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)