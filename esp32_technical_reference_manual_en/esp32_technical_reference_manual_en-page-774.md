Title: Revision History

Subtitle: Cont'd from previous page

Table:
- Column Headers: Date, Version, Release notes
- Row (First Entry):
  - Date: [2023.07]
  - Version: v5.0
  - Release notes: 
    - Updated register prefix APB_CTRL to SYSCON
    - Section **3.3.4 Cache**: Added description that the cache block size is 32 bytes
    - Chapter *6 IO MUX and GPIO Matrix* (GPIO, IO MUX): Split the original RTIO_TOUCH_PADn_REG (n: 0-9) into RTCIO TOUCH_PADn REG (n: 0-7) and RTCIO TOUCH_PADm REG (m: 8-9); In RTCIO TOUCH_PADn REG (n: 0-7), added bits [27-31], [12-16]
    - Revised Section *6.5.2 Analog Function Description*
    - Chapter **12 DPort Registers**: Added description of two registers DPRT_PRO_CACHE_CTRL1_REG and DPRT_APP_CACHE_CTRL1_REG
    - Section 12.3.7 Peripheral Clock Gating and Reset: Added a note about enabling clock and releasing reset state before using a peripheral
    - Section *2.5 SPI DMA Interface*: Changed the data size for a single transfer to “four bytes aligned”
    - Chapter **24 Ethernet Media Access Controller (EMAC)**: Removed contents about timestamp/PTP, as the feature is not supported in hardware
    - Chapter 23 Pulse Count Controller (PCNT): Added the description about the PCNT_CLK_EN bit

- Row (Second Entry):
  - Date: [2023.04]
  - Version: v4.9
  - Release notes:
    - Removed contents about hall sensor, including relevant registers, signals, etc to **PCN20212202**
    - Renamed PLL_D2_CLK to PLL_F160M_CLK throughout the document
    - Chapter *6 IO MUX and GPIO Matrix* (GPIO, IO MUX): Added TWAI signals in Table 6.9-1
    - Added descriptions about the break condition and updated maximum length of stop bits and related descriptions in Chapter **19 UART Controller** (UART)
    - Added the formula to calculate duty cycle resolution and updated Table Commonly-used Frequencies and Resolutions in Chapter *28 LED PWM Controller* (LEDC)
    - Chapter 31 On-Chip Sensors and Analog Signal Processing:
      - Added a note about limited applications of touch sensor in Section **31.2.2 Features**
      - Removed internal signals vdd33, pa_pkdet1, pa_pkdet2
    - Added description about “reject sleep” in Chapter *9 Low-Power Management* (RTC_CNTL)

Footer:
- Page number: 774
- Document version note: ESP32 TRM (Version 5.6)
- Link text: Submit Documentation Feedback

Navigation Links:
- GoBack button at the top right corner.
- "Cont'd on next page" link below each table entry.

Company Information:
- Espressif Systems logo and name are present in the bottom left of the document.