Title: Peripherals

Subtitle: Via IO MUX:
- Interface 4c is multiplexed with GPIO9 ~ GPIO14, RTC_GPIO9 ~ RTC_GPIO14, Touch Sensor interface, SAR ADC interface, and SPI interfaces 4d and 4g via IO MUX. It is the SPI2 main interface for fast SPI connection.
* (not recommended) Interface 4f is multiplexed with GPIO33 ~ GPIO38, SPI interfaces 4e and 4b via IO MUX. It is the alternative SPI2 interface if the main SPI2 is not available. Its performance is comparable to SPI2 via GPIO matrix, so use the GPIO matrix instead.
* (not recommended) Interface 4g is multiplexed with GPIO10 ~ GPIO14, RTC_GPIO10 ~ RTC_GPIO14, Touch Sensor interface, SAR ADC interface, and SPI interfaces 4c and 4d via IO MUX. It is the alternative SPI2 interface signal lines for 8-line SPI connection.

Subtitle: Via GPIO Matrix:
- The pins used can be chosen from any GPIOs via the GPIO Matrix.
- SPI3: The pins used can be chosen from any GPIOs via the GPIO Matrix

For more information about the pin assignment, see [ESP32-S3 Series Datasheet](#) > Section IO Pins and ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

Subtitle: 5.2.1.6 Two-Wire Automotive Interface (TWAI®)
The Two-Wire Automotive Interface (TWAI®) is a multi-master, multi-cast communication protocol with error detection and signaling as well as inbuilt message priorities and arbitration.

Title: Feature List
- Compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- Standard frame format (11-bit ID) and extended frame format (29-bit ID).
- Bit rates from 1 Kbit/s to 1 Mbit/s.
- Multiple modes of operation:
  - Normal
  - Listen Only
  - Self-Test (no acknowledgment required)
- 64-byte receive FIFO
- Acceptance filter (single and dual filter modes)
- Error detection and handling:
  - Error counters
  - Configurable error interrupt threshold
  - Error code capture
  - Arbitration lost capture

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter Two-wire Automotive Interface.

Footer: Espressif Systems  
Page number: 22  
Link: Submit Documentation Feedback