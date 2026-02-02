Title: Peripherals

- automatic padding data and discarding the padded data on the SDIO bus
- block size up to 512 bytes
- interrupt vector between the host and slave for bidirectional interrupt
- support DMA for data transfer
- support wake-up from sleep when connection is retained

For more details about the SDIO Slave controller, refer to the [ESP32-C5 Technical Reference Manual](#) > Chapter SDIO Slave Controller (SDIO).

Subtitle: Pin Assignment

The pins for the SDIO Slave controller are multiplexed with GPIO7 ~ GPIO10, GPIO13, and GPIO14 via IO MUX. GPIO13 ~ GPIO14 are also multiplexed with the pins for the USB serial/JTAG controller. The SDIO Slave controller can be used together with the USB Serial/JTAG controller in single SPI mode, but not in quad SPI mode.

For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section IO Pins and [ESP32-C5 Technical Reference Manual](#) > Chapter 10 MUX and GPIO Matrix.

Note:
This peripheral is not supported by chip revision v0.0 and v0.1.

Subtitle: 5.2.2 Analog Signal Processing

This subsection describes components on the chip that sense and process real-world data.

Subtitle: 5.2.2.1 Temperature Sensor

ESP32-C5 provides a temperature sensor to monitor temperature changes inside the chip in real time. The sensor converts analog voltage to digital values and supports compensation for the temperature offset.

Feature List
- software-triggered temperature measurement. Once triggered, the sensor continuously measures temperature. Software can read the data any time.
- hardware-triggered automatic temperature monitoring
- two modes for automatic monitoring of temperature and support for triggering interrupts
- configurable temperature offset based on the application scenario for improved accuracy
- configurable temperature measurement range
- support for several Event Task Matrix (ETM) related events and tasks

For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Temperature Sensor.

Subtitle: 5.2.2.2 ADC Controller

ESP32-C5 integrates One 12-bit successive approximation ADC (SAR ADC) for measuring analog signals from up to six channels.

Footer:
- Page number and document information at the bottom of each page.
- "Submit Documentation Feedback" link
- "PRELIMINARY" label indicating that this is a preliminary version.