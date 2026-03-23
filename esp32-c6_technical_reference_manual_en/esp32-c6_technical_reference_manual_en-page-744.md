

```markdown
## 27.4.9.1 Hardware Flow Control

Figure 27.4-8 shows the hardware flow control of a UART controller. Hardware flow control uses output signal `rtsn_out` and input signal `dsrn_in`. Figure 27.4-9 illustrates how these signals are connected between UART on ESP32-C6 (hereinafter referred to as IUO) and the external UART (hereinafter referred to as EUO).

When `rtsn_out` of IUO is low, EUO is allowed to send data. When `rtsn_out` of IUO is high, EUO is notified to stop sending data until `rtsn_out` of IUO returns to low. The output signal `rtsn_out` can be controlled in two ways.

- Software control: Enter this mode by clearing `UART_RX_FLOW_EN` to 0. In this mode, the level of `rtsn_out` is changed by configuring `UART_SW_RTS`.
- Hardware control: Enter this mode by setting `UART_RX_FLOW_EN` to 1. In this mode, `rtsn_out` is pulled high when data in Rx_FIFO exceeds `UART_RX_FLOW_THRHDD`.
```

Figure 27.4-8. Hardware Flow Control Diagram
```