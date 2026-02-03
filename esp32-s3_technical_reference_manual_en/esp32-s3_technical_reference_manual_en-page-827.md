**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Body Text:**
- Register `SYSTEM_CORE_1_CONTROL_1_REG` is used to facilitate the communication between CPU0 and CPU1. To be more specific, one CPU can write this register, using the agreed-on formats, which will then be read by the other CPU, thus achieving communication between these two CPUs. Note that the value in this register will not affect any hardware configuration, which allows CPU communication solely controlled by software.

**Footer:**
Espressif Systems
827 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Link Texts:**
- GoBack