**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header:**
Register 646. RTCIO_DIG_PAD_HOLD_REG (0x0074)

**Body Text:**
RTCIO_DIG_PAD_HOLD_REG Selects the digital pins which should be put on hold. While 0 allows normal operation, 1 puts the pin on hold.

**Table Title and Description:**
Table 6.13-1. Mapping of Bits to Pins

| Name       | Description                                                                 |
|------------|-----------------------------------------------------------------------------|
| Bit[0]     | Set to 1 to enable the Hold function of pin UORXD                           |
| Bit[1]     | Set to 1 to enable the Hold function of pin UOTXD                           |
| Bit[2]     | Set to 1 to enable the Hold function of pin SD_CLK                            |
| Bit[3]     | Set to 1 to enable the Hold function of pin SD_DATA0                          |
| Bit[4]     | Set to 1 to enable the Hold function of pin SD_DATA1                          |
| Bit[5]     | Set to 1 to enable the Hold function of pin SD_DATA2                          |
| Bit[6]     | Set to 1 to enable the Hold function of pin SD_DATA3                          |
| Bit[7]     | Set to 1 to enable the Hold function of pin SD_CMD                            |
| Bit[8]     | Set to 1 to enable the Hold function of pin GPIO5                             |
| Bit[9]     | Set to 1 to enable the Hold function of pin GPIO16                            |
| Bit[10]    | Set to 1 to enable the Hold function of pin GPIO17                            |
| Bit[11]    | Set to 1 to enable the Hold function of pin GPIO18                            |
| Bit[12]    | Set to 1 to enable the Hold function of pin GPIO19                            |
| Bit[13]    | Set to 1 to enable the Hold function of pin GPIO20                             |
| Bit[14]    | Set to 1 to enable the Hold function of pin GPIO21                            |
| Bit[15]    | Set to 1 to enable the Hold function of pin GPIO22                            |
| Bit[16]    | Set to 1 to enable the Hold function of pin GPIO23                            |

**Note:**
1. GPIO20 is only available for ESP32-PICO-V3 and ESP32-PICO-V3-02. Please refer to ESP32-PICO Series Datasheet for more information.

**Footer Information:**
Espressif Systems
Page 154 of ESP32 TRM (Version 5.6)
Submit Documentation Feedback