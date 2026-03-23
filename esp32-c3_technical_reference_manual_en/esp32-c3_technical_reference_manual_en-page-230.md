

```markdown
Chapter 9 Low-power Management

The boot flow after ESP32-C3 wakeup is shown in Figure 9.6-1.

Figure 9.6-1. ESP32-C3 Boot Flow

Wakes up
↓
Running in ROM
reset_vector@0x40000400
↓
Initialization
↓
Cal CRC in fast RTC mem
↓
CRC right? (Yes/No)
├─ Yes → Jump to entry point in RTC fast mem → Running in RTC fast mem → Return?
└─ No  → SPI Boot → Run code in CPU RAM → Running in CPU RAM

Espressif Systems                           230
ESP32-C3 TRM (Version 1.3)

Submit Documentation Feedback
```