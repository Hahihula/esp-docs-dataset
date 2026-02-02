**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Figure Caption:**
Figure 6.8-2. ESP32 I/O Pin Power Sources (QFN 5*5, Top View)

**Legend in Figure:**
- Pins marked blue are RTC pins that have their individual analog function and can also act as normal digital IO pins.
- For details about the power sources please see Section [6.11](#).
- Pins marked yellow and green have digital functions only.

**Subsection Title:**
6.8.1 VDD_SDIO Power Domain

**Body Text in Subsection:**
VDD_SDIO can source or sink current, allowing this power domain to be powered externally or internally. To power VDD_SDIO externally, apply the same power supply of VDD3P3, RTC to the VDD_SDIO pin.

Without an external power supply, the internal regulator will supply VDD_SDIO. The VDD_SDIO voltage can be configured to be either 1.8V or the same as VDD3P3_RTC, depending on the state of the MTDI pin at reset – a high level configures 1.8V and a low level configures the voltage to be the same as VDD3P3_RTC. Setting the efuse bit determines the default voltage of the VDD_SDIO. In addition, software can change the voltage of the VDD_SDIO by configuring register bits.

**Footer:**
Espressif Systems
123
ESP32 TRM (Version 5.6)

**Navigation Links:**
GoBack

**Feedback Link:**
Submit Documentation Feedback