**Chapter 6: IO MUX and GPIO Matrix (GPIO, IO MUX)**

- **GoBack**

---

### Notes:
- The output signal from a single peripheral can be sent to multiple pins simultaneously.
- Only the 28 GPIOs can be used as outputs.

The output signal can be inverted by setting the GPIO_FUNCx_OUT_INV_SEL bit.

**6.3.3 Simple GPIO Output**
The GPIO Matrix can also be used for simple GPIO output – setting a bit in the GPIO_OUT_DATA register will write to the corresponding GPIO pin.
To configure a pin as simple GPIO output, the GPIO Matrix GPIO_FUNCx_OUTSEL register is configured with a special peripheral index value (0x100).

**6.4 Direct I/O via IO MUX**
- **6.4.1 Summary**
  Some high speed digital functions (Ethernet, SDIO, SPI, JTAG, UART) can bypass the GPIO Matrix for better high-frequency digital performance. In this case, the IO MUX is used to connect these pins directly to the peripheral.
  Selecting this option is less flexible than using the GPIO Matrix, as the IO MUX register for each GPIO pin can only select from a limited number of functions. However, better high-frequency digital performance will be maintained.

- **6.4.2 Functional Description**
  Two registers must be configured in order to bypass the GPIO Matrix for peripheral I/O:
  - IO MUX for the GPIO pin must be set to the required pin function.
    (Please refer to section [6.10](#) for a list of pin functions.)
  - For inputs, the SIG_IN_SEL register must be cleared to route the input directly to the peripheral.

**6.5 RTC IO MUX for Low Power and Analog I/O**
- **6.5.1 Summary**
  18 GPIO pins have low power capabilities (RTC domain) and analog functions which are handled by the RTC subsystem of ESP32.
  The IO MUX and GPIO Matrix are not used for these functions; rather, the RTC_MUX is used to redirect the I/O to the RTC subsystem.

---

**Espressif Systems**
**120**
**ESP32 TRM (Version 5.6)**
**Submit Documentation Feedback**