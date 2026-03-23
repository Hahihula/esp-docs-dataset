

```markdown
## 26.4.9 Flow Control

UART controllers have two ways to control data flow, namely hardware flow control and software flow control.
Hardware flow control is achieved using output signal `rtsn_out` and input signal `dsrn_in`. Software flow control is achieved by inserting special characters in the data flow sent and detecting special characters in the data flow received.

### 26.4.9.1 Hardware Flow Control

![Figure 26.4-9. Hardware Flow Control Diagram](image_path)

Figure 26.4-9 shows the hardware flow control of a UART controller. Hardware flow control uses output signal `rtsn_out` and input signal `dsrn_in`. Figure 26.4-10 illustrates how these signals are connected between UART on ESP32-C3 (hereinafter referred to as IUO) and the external UART (hereinafter referred to as EUO).

When `rtsn_out` of IUO is low, EUO is allowed to send data; when `rtsn_out` of IUO is high, EUO is notified to stop sending data until `rtsn_out` of IUO returns to low. The output signal `rtsn_out` can be controlled in two ways.

*   Software control: Enter this mode by clearing `UART_RX_FLOW_EN` to 0. In this mode, the level of `rtsn_out` is changed by configuring `UART_SW_RTS`.
*   Hardware control: Enter this mode by setting `UART_RX_FLOW_EN` to 1. In this mode, `rtsn_out` is pulled high when data in Rx_FIFO exceeds `UART_RX_FLOW_THRHDD`.
```