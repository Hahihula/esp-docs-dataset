**Title: Peripherals**

- Special character AT_CMD detection
- RS485 protocol
- IrDA protocol
- High-speed data communication using GDMA
- UART as wake-up source
- Software and hardware flow control

For details, see [ESP32-S3 Technical Reference Manual > Chapter UART Controller](http://example.com).

---

**Title: Pin Assignment**

#### UART0

- The pins UOTXD and UORXD that are connected to transmit and receive signals are multiplexed with GPIO43 ~ GPIO44 via IO MUX, and can also be connected to any GPIO via the GPIO Matrix.

- The pins UORTS and UOCTS that are connected to hardware flow control signals are multiplexed with GPIO15 ~ GPIO16, RTC_GPIO15 ~ RTC_GPIO16, XTAL_32K_P and XTAL_32K_N, and SAR ADC2 interface via IO MUX, and can also be connected to any GPIO via the GPIO Matrix.

- The pins UODTR and UODSR that are connected to hardware flow control signals can be chosen from any GPIO via the GPIO Matrix.

#### UART1

- The pins UIUTXD and UIURXD that are connected to transmit and receive signals are multiplexed with GPIO17 ~ GPIO18, RTC_GPIO17 ~ RTC_GPIO18, and SAR ADC2 interface via IO MUX, and can also be connected to any GPIO via the GPIO Matrix.

- The pins UIRTS and UICTS that are connected to hardware flow control signals are multiplexed with GPIO19 ~ GPIO20, RTC_GPIO19 ~ RTC_GPIO20, USB_D- and USB_D+ pins, and SAR ADC2 interface via IO MUX, and can also be connected to any GPIO via the GPIO Matrix.

- The pins UIUTDR and UIUDSR that are connected to hardware flow control signals can be chosen from any GPIO via the GPIO Matrix.

#### UART2

The pins used can be chosen from any GPIO via the GPIO Matrix. For more information about the pin assignment, see [ESP32-S3 Series Datasheet > Section IO Pins and ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](http://example.com).

---

**Title: 5.2.1.2 I2C Interface**

ESP32-S3 has two I2C bus interfaces which are used for I2C master mode or slave mode, depending on the user’s configuration.

**Feature List**
- Standard mode (100 kbit/s)
- Fast mode (400 kbit/s)
- Up to 800 kbit/s (constrained by SCL and SDA pull-up strength)

---

**Footer:**

Espressif Systems  
Page number: 18  
Submit Documentation Feedback

ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6