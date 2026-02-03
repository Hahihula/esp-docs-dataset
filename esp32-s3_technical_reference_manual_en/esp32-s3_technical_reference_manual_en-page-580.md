**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Table Title and Source Note:**
Table 10.4-3. Wakeup Source

**Table Content:**

| WAKEUP_ENA | Wakeup Source^10 | Light-sleep | Deep-sleep | Note |
|-------------|------------------|-------------|------------|------|
| 0x1         | EXTO             | Y           | Y          | 1    |
| 0x2         | EXT1            | Y           | -          | 2    |
| 0x4         | GPIO             | Y           | Y          | 3    |
| 0x8         | RTC timer        | Y           | -          |      |
| 0x20        | Wi-Fi            | Y           | -          | 4    |
| 0x40        | UARTO            | Y           | -          | 5    |
| 0x80        | UART1            | Y           | -          | 5    |
| 0x100       | TOUCH Active     | Y           | Y          | 6    |
| 0x200       | ULP-FSM          | Y           | -          | 7    |
| 0x400       | BT               | Y           | -          | 4    |
| 0x800       | ULP-RISC-V       | Y           | -          |      |
| 0x1000      | XTAL_32K         | Y           | Y          | 8    |
| 0x2000      | ULP-RISC-V Trap  | Y           | -          | 9    |
| 0x8000      | TOUCH Timeout    | Y           | -          |-     |
| 0xc000      | BROWNOUT         | Y           | -          |-     |

**Notes:**
1. EXTO can only wake up the chip from Light-sleep/Deep-sleep modes.
2. EXT1 is especially designed to wake up the chip from any sleep modes, and can be triggered by a combination of pins. Users should define the combination of wakeup sources by configuring RTC_CNTL_EXT_WAKEUP1_SEL[17:0] according to the bitmap of selected wakeup source. When RTC_CNTL_EXT_WAKEUP1_LV == 1, the chip is waken up if any pin in the combination is high level.
3. In Deep-sleep mode, only the RTC GPIOs (not regular GPIOs) can work as a wakeup source.

**Additional Notes:**
- The CPU and radio are woken up at predetermined intervals to keep Wi-Fi/Bluetooth connections active.
- A wakeup is triggered when any touch event is detected by the touch sensor. 
- When the 32 kHz crystal is working as RTC slow clock, a wakeup is triggered upon detection of any crystal stops or by the 32 kHz watchdog timer.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32-S3 TRM (Version 1.7)