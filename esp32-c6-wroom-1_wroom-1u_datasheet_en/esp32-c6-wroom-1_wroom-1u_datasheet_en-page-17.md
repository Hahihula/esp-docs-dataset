Title: Peripherals

Subtitle: Functional Overview (5.1)

Body Text:
ESP32-C6 integrates a rich set of peripherals including SPI, parallel IO interface, UART, I2C, I2S, RMT (TX/RX), LED PWM, USB Serial/JTAG controller, MCPWM, SDIO slave controller, GDMA, TWAI® controller, on-chip debug functionality via JTAG, event task matrix, ADC, as well as up to 23 GPIOs, etc.

For detailed information about module peripherals, please refer to ESP32-C6 Series Datasheet > Section Functional Description. Note that the ADC measurement range and accuracy in the ESP32-C6 Series Datasheet are applicable to modules manufactured on and after the PW Number PW-2023-07-XXX on packaging labels. For modules manufactured earlier than these PW numbers, please ask our sales team to provide the actual range and accuracy according to batches.

Note:
The content below is excerpted from ESP32-C6 Series Datasheet > Section Peripherals. Some information may not be applicable to ESP32-C6-WROOM-1 and ESP32-C6-WROOM-1U as not all the IO signals are exposed on the module.
To learn more details about peripherals, please refer to ESP32-C6 Technical Reference Manual > Section Peripheral Signal List.

Subtitle: Peripheral Description (5.2)

Body Text:
This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

Subtitle: Connectivity Interface

Sub-subtitle: UART Controller
(5.2.1.1)

Body Text:
The UART Controller in the ESP32-C6 chip facilitates the transmission and reception of asynchronous serial data between the chip and external UART devices. It consists of two UARTs in the main system, and one low-power LP UART.

Feature List:

- Programmable baud rates up to 5 Mbaud
- RAM shared by TX FIFOs and RX FIFOs
- Support for various lengths of data bits and stop bits
- Parity bit support
- Special character AT_CMD detection
- RS485 protocol support (not supported by LP UART)
- IrDA protocol support (not supported by LP UART)

Footer:
Espressif Systems 17 ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4

Link: Submit Documentation Feedback