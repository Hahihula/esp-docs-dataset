**Title: Chapter 26 UART Controller (UART)**

---

### Figure Caption:
- **Figure 26.4-2. UART Controllers Division**

---

#### Body Text:

To support IrDA (see Section 26.4.7 for details), the fractional clock divider for IrDA data transmission generates clock signals divided by 16 × UART_CLKDIV_REG. This divider works similarly as the one elaborated above: it takes UART_CLKDIV/16 as the integer value and the lowest four bits of UART_CLKDIV as the fractional value.

---

#### Subtitle:
**26.4.3.2 Baud Rate Detection**

---

#### Body Text:

Automatic baud rate detection (Autobaud) on UARTs is enabled by setting UART_AUTOBAUD_EN. The Baudrate_Detect module shown in Figure 26.3-2 filters any noise whose pulse width is shorter than UART_GLITCH_FILTER.

Before communication starts, the transmitter can send random data to the receiver for baud rate detection.
- **UART_LOWPUULSE_MIN_CNT** stores the minimum low pulse width,
- **UART_HIGHPULSE_MIN_CNT** stores the minimum high pulse width,
- **UARTPOSEDGE_MIN_CNT** stores the minimum pulse width between two rising edges, and
- **UART_NEGEDGE_MIN_CNT** stores the minimum pulse width between two falling edges. These four fields are read by software to determine the transmitter’s baud rate.

---

#### Figure Caption:
- **Figure 26.4-3. The Timing Diagram of Weak UART Signals Along Falling Edges**

---

#### Body Text:

The baud rate can be determined in the following three ways:
1. Normally, to avoid sampling erroneous data along rising or falling edges in a metastable state, which results in the inaccuracy of UART_LOWPUULSE_MIN_CNT or UART_HIGHPULSE_MIN_CNT, use a weighted average of these two values to eliminate errors. In this case, the baud rate is calculated as follows:
\[ B_{\text{uart}} = \frac{f_{\text{clk}}}{(\text{UART_LOWPUULSE_MIN_CNT} + \text{UART_HIGHPULSE_MIN_CNT} + 2)/2} \]

2. If UART signals are weak along falling edges as shown in Figure 26.4-3, which leads to an inaccurate average of UART_LOWPUULSE_MIN_CNT and UART_HIGHPULSE_MIN_CNT, use

---

**Footer:**
Espressif Systems  
929  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback]