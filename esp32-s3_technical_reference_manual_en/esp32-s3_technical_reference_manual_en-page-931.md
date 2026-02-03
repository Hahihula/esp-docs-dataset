Title: Chapter 26 UART Controller (UART)

Subtitle: 26.4.5 AT_CMD Character Structure

Figure Caption:
- Figure 26.4-5. AT_Cmd Command Structure

Body Text:

Figure 26.4-5 is the structure of a special character AT_CMD. If the receiver constantly receives AT_CMD_CHAR and the following conditions are met, a UART_AT.Cmd_CHAR_DET_INT interrupt is generated.
The specific value of AT_CMD_CHAR can be read from UARTn_AT_Cmd_CHAR.

- The interval between the first AT_CMD_CHAR and the last non-AT_CMD_CHAR character is at least UART_PRE_IDLE_NUM cycles.
  
- The interval between two AT_CMD_CHAR characters is less than UART_RX_GAP_TOUT cycles.
  
- The number of AT_CMD_CHAR characters is equal to or greater than UART_CHAR_NUM.
  
- The interval between the last AT_CMD_CHAR character and next non-AT_Cmd_CHAR character is at least UART_POST_IDLE_NUM cycles.

Subtitle: 26.4.6 RS485

Body Text:

All three UART controllers support RS485 protocol. This protocol uses differential signals to transmit data, so it can communicate over longer distances at higher bit rates than RS232. RS485 has two-wire half-duplex mode and four-wire full-duplex modes. UART controllers support two-wire half-duplex transmission and bus snooping. In a two-wire RS485 multidrop network, there can be 32 slaves at most.

Subtitle: 26.4.6.1 Driver Control

Body Text:

As shown in Figure 26.4-6, in a two-wire multidrop network, an external RS485 transceiver is needed for differential to single-ended conversion. An RS485 transceiver contains a driver and a receiver. When a UART controller is not in transmitter mode, the connection to the differential line can be broken by disabling the driver. When the DE (Driver Enable) signal is 1, the driver is enabled; when DE is 0, the driver is disabled.

The UART receiver converts differential signals to single-ended signals via an external receiver. RE is the enable control signal for the receiver. When RE is O, the receiver is enabled; when RE is 1, the receiver is disabled. If RE is configured as OD, the UART controller is allowed to snoop data on the bus, including the data sent by itself.

DE can be controlled by either software or hardware. To reduce the cost of software, DE is controlled by hardware in our design. As shown in Figure 26.4-6, DE is connected to dtrn_out of UART (please refer to Section 26.4.10.1 for more details).

Footer:
- Espressif Systems
- Page number: 931
- Document version and feedback link: ESP32-S3 TRM (Version 1.7) Submit Documentation Feedback