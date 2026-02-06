Title: Peripherals

Body Text:
- All channels share an RX FIFO, non-periodic TX FIFO, and periodic TX FIFO. The size of each FIFO is configurable.
- For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter USB On-The-Go.

Subtitle: Pin Assignment
Body Text:
When using the on-chip PHY, the differential signal pins USB_D- and USB_D+ of the USB OTG are multiplexed with GPIO19 ~ GPIO20, RTC_GPIO19 ~ RTC_GPIO20, UART1 interface, and SARA ADC2 interface via IO MUX.

When using external PHY, the USB OTG pins are multiplexed with GPIO21, RTC_GPIO21, GPIO38 ~ GPIO42, and SPI interface via IO MUX:
- VP signal connected to MTMS pin
- VM signal connected to MTDI pin
- RCV signal connected to GPIO21
- OEN signal connected to MTDIO pin
- VPO signal connected to MTCK pin
- VMO signal connected to GPIO38

For more information about the pin assignment, see [ESP32-S3 Series Datasheet](#) > Section IO Pins and [ESP32-S3 Technical Reference Manual](#) > Chapter IO MUX and GPIO Matrix.

Subtitle: 5.2.1.8 USB Serial/JTAG Controller
Body Text:
ESP32-S3 integrates a USB Serial/JTAG controller.
- For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter USB Serial/JTAG Controller

Subtitle: Feature List
List Items:
- USB Full-speed device.
- Can be configured to either use internal USB PHY of ESP32-S3 or external PHY via GPIO matrix.
- Fixed function device, hardwired for CDC-ACM (Communication Device Class - Abstract Control Model) and JTAG adapter functionality.
- Two OUT Endpoints, three IN Endpoints in addition to Control Endpoint; Up to 64-byte data payload size.
- Internal PHY, so no or very few external components needed to connect to a host computer.
- CDC-ACM adherent serial port emulation is plug-and-play on most modern OSes.
- JTAG interface allows fast communication with CPU debug core using a compact representation of JTAG instructions.
- CDC-ACM supports host controllable chip reset and entry into download mode.

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter USB Serial/JTAG Controller

Footer:
Espressif Systems
Page Number: 24
Document Title: ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6