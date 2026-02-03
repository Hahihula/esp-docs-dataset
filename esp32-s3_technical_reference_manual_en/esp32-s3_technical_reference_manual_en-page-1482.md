**Title: Chapter 39 On-Chip Sensors and Analog Signal Processing**

**Subtitle: Register 39.2. RTC_CNTL_TOUCH_CTRL2_REG (0x10C)**

Continued from the previous page...

- **RTC_CNTL_TOUCH_SLP_CYC_DIV**: When a touch pin is active, sleep cycle could be divided by this number.
  - Access type: Read/Write
- **RTC_CNTL TOUCH TIMER FORCE DONE**: Force touch timer force done. (Read/Write)
- **RTC_CNTL_TOUCH_RESET**: Reset touch FSM via software. (Read/Write)
- **RTC_CNTL_TOUCH_CLK_FO**: Touch clock force on. (Read/Write)
- **RTC_CNTL_TOUCH_CLKGATE_EN**: Touch clock enable bit.
  - Access type: Read/Write

**Subtitle: Register 39.3. RTC_CNTL TOUCH SCAN CTRL REG (0x110)**

| Bit Field | Description |
|-----------|-------------|
| 31        | Oxf         |
| 28        | OxO         |
| 27-24     | 0x00        |
| ...       | ...         |

**Field Details:**

- **RTC_CNTL_TOUCH_DENOISE_RES**: De-noise resolution.
  - Access type: Read/Write
  - Options:
    - O: 12-bit (Read)
    - I: 10-bit (Read)
    - Z: 8-bit (Read)
    - D: 4-bit (Read)

- **RTC_CNTL_TOUCH_DENOISE_EN**: Touch pin 0 will be used to de-noise.
  - Access type: Read/Write

- **RTC_CNTL_TOUCH_INACTIVE_CONNECTION**: Inactive touch pins connect to:
  - GND, O: HighZ. 
  - Access type: Read/Write
- **RTC_CNTL_TOUCH_SHIELD_PAD_EN**: Touch pin 14 will be used as shield pin.
  - Access type: Read/Write

- **RTC_CNTL_TOUCH_SCAN_PAD_MAP**: Pin enable map for touch scan mode.
  - Access type: Read/Write

- **RTC_CNTL TOUCH BUFDRV**: Touch buffer driver strength. (Read/Write)
- **RTC_CNTL_TOUCH_OUT_RING**: Select one pin as guard_ring.

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7) 
- Page Number: 1482

[Submit Documentation Feedback](#)