Title: Chapter 26 UART Controller (UART)

Body Text:
Figure **26.3-2** shows the basic structure of a UART controller. A UART controller works in two clock domains, namely APB_CLK domain and Core Clock domain (the UART Core’s clock domain). The UART Core has three clock sources: 80 MHz APB_CLK, RC_FAST_CLK and external crystal clock XTAL_CLK (for details, please refer to Chapter **7 Reset and Clock**), which are selected by configuring **UART_SCLK_SEL**. The selected clock source is divided by a divider to generate clock signals that drive the UART Core.

A UART controller is broken down into two parts: a transmitter and a receiver.

The transmitter contains a FIFO, called TX_FIFO (or Tx_FIFO), which buffers data to be sent. Software can write data to the Tx_FIFO either via the APB bus, or using DMA. Tx_FIFO Ctrl controls writing and reading the Tx_FIFO. When Tx_FIFO is not empty, Tx_FSM reads data bits in the data frame via Tx_FIFO_Ctrl, and converts them into a bitstream. The levels of output signal txd_out can be inverted by configuring the **UART_TXD_INV** field.

The receiver also contains a FIFO, called RX_FIFO (or Rx_FIFO), which buffers received data. The levels of input signal rxd_in can be inverted by configuring **UART_RXD INV** field. Baudrate_Detect measures the baud rate of input signal rxd_in by detecting its minimum pulse width. Start_Detect detects the start bit in a data frame. If the start bit is detected, Rx_FSM stores data bits in the data frame into Rx_FIFO by Rx_FIFO_Ctrl. Software can read data from Rx_FIFO via the APB bus, or receive data using DMA.

HW_Flow_Ctrl controls rxd_in and txd_out data flows by standard UART RTS and CTS flow control signals (rtsn_out and ctsn_in). SW_Flow_Ctrl controls data flows by automatically adding special characters to outgoing data and detecting special characters in incoming data.
When a UART controller is in Light-sleep mode (see Chapter **10 Low-power Management (RTC_CNTL)** for more details), Wakeup_Ctrl counts up rising edges of rxd_in. When the number is equal to or greater than **UART_ACTIVE_THRESHOLD** + 3, a wake_up signal is generated and sent to RTC, which then wakes up the ESP32-S3 chip.

Subtitle: Section Heading

Title: 26.4 Functional Description

Subtitle: Subsection Title within Section

Title: 26.4.1 Clock and Reset

Body Text:
UART controllers are asynchronous. their configuration registers, TX FIFOs, and RX FIFOs are in APB_CLK domain, while the module controlling transmission and reception (i.e., UART Core) is in Core Clock domain.

The latter can be sourced out of three clocks, namely APB_CLK, RC_FAST_CLK and external crystal clock XTAL_CLK, which can be selected by configuring **UART_SCLK_SEL**. The selected clock source can be divided. This divider supports fractional division, and the divisor is equal to:

\[ \text{UART_SCLK_DIV_NUM} + \frac{\text{UART_SCLK_DIV_DV_B}}{\text{UART_SCLK_DIV_A}} \]

The divisor ranges from 1 ~ 256.

When the frequency of the UART Core’s clock is higher than the frequency needed to generate the baud rate, the UART Core can be clocked at a lower frequency by the divider, in order to reduce power consumption. Usually, the UART Core's clock frequency is lower than the APB_CLK’s frequency, and can be divided by the largest divisor value when higher than the frequency needed to generate the baud rate. The frequency of the UART Core’s clock can also be at most twice higher than the APB_CLK. The clock for the UART transmitter and the UART receiver can be controlled independently. To enable the clock for the UART transmitter,

Footer: Espressif Systems
Page Number: 926

Link Text:
GoBack

Submit Documentation Feedback