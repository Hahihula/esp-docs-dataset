Title: Functional Description

- Supports signal synchronization for peripheral inputs based on APB clock bus
- Provides input signal filter
- Supports sigma delta modulated output
- Supports GPIO simple input and output

Subtitle: IO MUX:

- Provides one configuration register `IO_MUX_GPIO_n_REG` for each GPIO pin. The pin can be configured to:
  * perform GPIO function routed by GPIO matrix
  * or perform direct connection bypassing GPIO matrix

- Supports some high-speed digital signals (SPI, JTAG, UART) bypassing GPIO matrix for better high-frequency digital performance (IO MUX is used to connect these pins directly to peripherals)

Subtitle: RTC IO MUX:

- Controls low power feature of 22 RTC GPIO pins
- Controls analog functions of 22 RTC GPIO pins
- Redirects 22 RTC input/output signals to RTC system

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter IO MUX and GPIO Matrix.

Subtitle: Reset (Section)

ESP32-S3 provides four reset levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset.

### Feature List
- Support for four reset levels:
  - **CPU Reset:** only resets CPUs `core`. CPUs can be CPU0 or CPU1 here. Once such reset is released, programs will be executed from CPU `reset vector`. Each CPU core has its own reset logic. If CPU Reset is from CPU0, the sensitive registers will be reset, too.
  - Core Reset: resets the whole digital system except RTC, including CPU0, CPU1, peripherals, Wi-Fi, Bluetooth® LE (BLE), and digital GPIOs.
  - System Reset: resets the whole digital system, including RTC.
  - Chip Reset: resets the whole chip.

- **Support software reset and hardware reset:**
  - Software reset is triggered by CPUs `configuring its corresponding registers`. Refer to [ESP32-S3 Technical Reference Manual](#) > Chapter Low-power Management for more details.
  - Hardware reset is directly triggered by the circuit.

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter Reset and Clock. 

Footer:
- Espressif Systems
- Submit Documentation Feedback

Document Version: ESP32-S3 Series Datasheet v2.1