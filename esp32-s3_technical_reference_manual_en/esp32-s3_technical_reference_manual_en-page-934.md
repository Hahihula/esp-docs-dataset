**Title:**
Chapter 26 UART Controller (UART)

**Body Text:**
ctsn_in, and dtrn_out is connected to dsrn_out. Data are then sent out through txd_out. If the data received match the data sent, it indicates that UART controller is working properly.

**Subtitle: Flow Control**

**Body Text:**
UART controllers have two ways to control data flow, namely hardware flow control and software flow control. Hardware flow control is achieved using output signal rtsn_out and input signal dsrn_in. Software flow control is achieved by inserting special characters (XON or XOFF) in the data flow sent and detecting special characters in the data flow received.

**Subtitle: 26.4.10.1 Hardware Flow Control**

**Diagram Description:**
Figure shows a hardware flow control diagram of a UART controller with various components such as UART_RX_FIFO_CNT, UART_RX_FLOW_THRD, UART_RX_FLOW_EN, UART_RTS_INV, UART LOOPBACK, UART_CTS_INV, UART_DTR INV, UART_RS485_EN.

**Caption for Diagram:**
Figure 26.4-9 shows the hardware flow control of a UART controller. Hardware flow control uses output signal rtsn_out and input signal dsrn_in.
Figure illustrates how these signals are connected between UART on ESP32-S3 (hereinafter referred to as IUO) and the external UART (hereinafter referred to as EUO).

**Additional Information:**
When rtsn_out of IUO is low, EUO is allowed to send data; when rtsn_out of IUO is high, EUO is notified to stop sending data until rtsn_out of IUO returns to low. The output signal rtsn_out can be controlled in two ways.

- **Software control:** Enter this mode by clearing UART_RX_FLOW_EN to 0. In this mode, the level of rtsn_out is changed by configuring UART_SW_RTS.
- **Hardware control:** Enter this mode by setting UART_RX_FLOW_EN to 1. In this mode, rtsn_out is pulled high when data in Rx_FIFO exceeds UART_RX_FLOW_THRD.

**Footer:**
Espressif Systems
934 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback