

```markdown
## 27.4.3.2 Baud Rate Detection

Automatic baud rate detection (Autobaud) on UARTs is enabled by setting `UART_AUTObAUD_EN`. The Baudrate_Detect module shown in Figure 27.3-1 filters any noise whose pulse width is shorter than `UART_GLITCH_FILT`.

Before communication starts, the transmitter could send random data to the receiver for baud rate detection. `UART_LOWPULSE_MIN_CNT` stores the minimum low pulse width, `UART_HIGHPULSE_MIN_CNT` stores the minimum high pulse width, `UART_POSEDGE_MIN_CNT` stores the minimum pulse width between two rising edges, and `UART_NEGEDGE_MIN_CNT` stores the minimum pulse width between two falling edges. These four fields are read by software to determine the transmitter's baud rate.

![Figure 27.4-2. The Timing Diagram of Weak UART Signals Along Falling Edges](image)

The baud rate can be determined in the following three ways:

1. Normally, to avoid sampling erroneous data along rising or falling edges in a metastable state, which results in the inaccuracy of `UART_LOWPULSE_MIN_CNT` or `UART_HIGHPULSE_MIN_CNT`, use a weighted average of these two values to eliminate errors for 1-bit pulses. In this case, the baud rate is calculated as follows:

    $$B_{\text{uart}} = \frac{f_{\text{clk}}}{(\text{UART_LOWPULSE\_MIN\_CNT} + \text{UART_HIGHPULSE\_MIN\_CNT} + 2)/2}$$

2. If UART signals are weak along falling edges as shown in Figure 27.4-2, which leads to an inaccurate average of `UART_LOWPULSE_MIN_CNT` and `UART_HIGHPULSE_MIN_CNT`, use `UART_POSEDGE_MIN_CNT` to determine the transmitter's baud rate as follows:

    $$B_{\text{uart}} = \frac{f_{\text{clk}}}{(\text{UART_POSEDGE\_MIN\_CNT} + 1)/2}$$

3. If UART signals are weak along rising edges, use `UART_NEGEDGE_MIN_CNT` to determine the transmitter's baud rate as follows:

    $$B_{\text{uart}} = \frac{f_{\text{clk}}}{(\text{UART_NEGEDGE\_MIN\_CNT} + 1)/2}$$
```