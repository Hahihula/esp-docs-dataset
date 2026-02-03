Title: Peripherals

Subtitle: 5.1 Peripheral Overview

Body Text:
ESP32-C5 integrates a rich set of peripherals including SPI, parallel IO interface, UART, I2C, I2S, RMT (TX/RX), pulse counter, LED PWM, USB Serial/JTAG controller, MCPWM, GDMA, CAN FD controller, SDIO slave controller, BitScrambler, event task matrix, ADC, temperature sensor, brownout detector, analog voltage comparator, as well as up to 22 GPIOs, etc.

To learn more about on-chip components, please refer to ESP32-C5 Series Datasheet > Section Functional Description

Note:
The content below is sourced from ESP32-C5 Series Datasheet > Section Peripherals. Some information may not be applicable to ESP32-C5-MINI-1 as not all the IO signals are exposed on the module.
To learn more about peripheral signals, please refer to ESP32-C5 Technical Reference Manual > Section Peripheral Signal List.

Subtitle: 5.2 Peripheral Description

Body Text:
This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

Subtitle: 5.2.1 Connectivity Interface

Body Text:
This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

Subtitle: 5.2.1.1 UART Controller

Body Text:
ESP32-C5 has three UART interfaces, i.e. UART0, UART1, and LP UART. All the three interfaces provide hardware flow control (CTS and RTS signals) and software flow control (XON and XOFF).

Feature List:

- programmable baud rates up to 5 Mbaud
- RAM shared by TX FIFOs and RX FIFOs
- support for various lengths of data bits and stop bits
- parity bit support
- special character AT_CMD detection
- RS485 protocol support (not supported by LP UART)
- IrDA protocol support (not supported by LP UART)
- high-speed data communication using GDMA (not supported by LP UART)
- receive timeout feature

Footer:
Espressif Systems 18 ESP32-C5-MINI-1 Datasheet v1.0
Submit Documentation Feedback