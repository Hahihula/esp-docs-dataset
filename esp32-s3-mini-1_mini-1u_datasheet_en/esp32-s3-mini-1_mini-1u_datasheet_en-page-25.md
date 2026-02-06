**Title: Peripherals**

---

### Pin Assignment

When using the on-chip PHY, the differential signal pins USB_D- and USB_D+ of the USB Serial/JTAG controller are multiplexed with GPIO19 ~ GPIO20, RTC_GPIO19 ~ RTC_GPIO20, UART1 interface, and SAR ADC2 interface via IO MUX.

When using external PHY, the USB Serial/JTAG controller pins are multiplexed with GPIO38 ~ GPIO42 and SPI interface via IO MUX:

- VP signal connected to MTMS pin
- VM signal connected to MTDI pin
- OEN signal connected to MTDO pin
- VPO signal connected to MTCK pin
- VMO signal connected to GPIO38

For more information about the pin assignment, see [ESP32-S3 Series Datasheet > Section IO Pins and ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

**Title: 5.2.1.9 SD/MMC Host Controller**

ESP32-S3 has an SD/MMC Host controller.

### Feature List

- Secure Digital (SD) memory version 3.0 and version 3.01
- Secure Digital I/O (SDIO) version 3.0
- Consumer Electronics Advanced Transport Architecture (CE-ATA) version 1.1
- Multimedia Cards (MMC version 4.4, eMMC version 4.5 and version 4.5i)
- Up to 80 MHz clock output
- Three data bus modes:
  - 1-bit
  - 4-bit (supports two SD/SDIO/MMC 4.4 cards, and one SD card operating at 1.8 V in 4-bit mode)
  - 8-bit

For details, see [ESP32-S3 Technical Reference Manual > Chapter SD/MMC Host Controller](#).

---

### Pin Assignment

For SD/MMC Host, the pins used can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-S3 Series Datasheet > Section IO Pins and ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

**Title: 5.2.1.10 LED PWM Controller**

The LED PWM controller can generate independent digital waveforms on eight channels.

[Footer]: 
- Page number: "25"
- Document title: "ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6"
- Link to submit documentation feedback

---