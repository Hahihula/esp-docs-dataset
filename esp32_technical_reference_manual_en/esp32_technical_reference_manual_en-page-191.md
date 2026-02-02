**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Table Title:**
Table 9.3-2. Wake-up Source

| WAKEUP_ENA | Wake-up Source^1 | Light-sleep | Deep-sleep | Hibernation |
|-------------|------------------|-------------|------------|-------------|
| 0x1         | EXTO^2          | Y           | Y         | -           |
| 0x2         | EXT1^3          | Y           | Y         | Y          |
| 0x4         | GPIO^4          | Y           | Y         | -          |
| 0x8         | RTC timer       | Y           | Y         | Y          |
| 0x10        | SDIO^5          | Y           | -         | -          |
| 0x20        | Wi-Fi^6         | Y           | -         | -          |
| 0x40        | UART0^7        | Y           | -         | -          |
| 0x80        | UART1^7        | Y           | -         | -          |
| 0x100       | TOUCH           | Y           | Y         | -          |
| 0x200       | ULP co-processor | Y           | -         | -          |
| 0x400       | BT^6            | -           | -         | -          |

**Body Text:**

1. The GPIO and SDIO wakeup sources can also be configured as the causes to reject sleep.
2. EXTO can only wake up the chip in light-sleep/deep-sleep mode.

   If RTC_CNTL_EXWAKEUPO_LV is 1, it is pad high-level triggered; otherwise, it is low-level triggered. Users can set RTCIOExWAKEUPOSEL[4:0] to select one of the RTC PADs to be the wake-up source.
3. EXT1 is especially designed to wake up the chip from any sleep mode, and it also supports multiple pads' combinations.

   First, RTC_CNTL_EXWAKEUP1_SEL[17:0] should be configured with the bitmap of PADS selected as a wake-up source. Then, if RTC_CNTL_EXWAKEUPO_LV is 1, as long as one of the PADS is at high-voltage level, it can trigger a wake-up. However, if RTC_CNTL_EXWAKEUP1_LV is O, it needs all selected PADS to be at low-voltage level to trigger a wake-up.

**Note:**
that the EXT1 hold time should longer than three RTC slow clock cycles, otherwise the signal status will not be captured in RTC_CNTL_EXWAKEUPO1_STATUS.
4. In Deep-sleep mode, only RTC GPIOs (not DIGITAL GPIOs) can work as wakeup source.
5. Wake-up is triggered by receiving any SDIO command.

6. To wake up the chip with a Wi-Fi or BT source, the power mode switches between the Active, Modem- and Light-sleep modes. The CPU, Wi-Fi, Bluetooth, and radio are woken up at predetermined intervals to keep Wi-Fi/BT connections active.
7. Wake-up is triggered when the number or positive edges of RxD signal is greater than or equal to (UART_ACTIVE_THRESHOLD+2). Note that the RxD signal cannot be input through GPIO Matrix but only through IO_MUX.

**Subsection Title:**
9.3.11 Reject Sleep

**Body Text for Subsection 9.3.11:**

ESP32 implements a hardware mechanism that equips the chip with the ability to reject sleep, which prevents the chip from going to sleep unexpectedly when some peripherals are still working but not detected.

**Footer Information:**
Espressif Systems  
Page Number: 191  
Document Title: ESP32 TRM (Version 5.6)  
Link Texts: Submit Documentation Feedback