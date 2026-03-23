

```markdown
## 29.3 I2C Architecture

Figure 29.3-1. I2C Master Architecture

Figure 29.3-2. I2C Slave Architecture

The I2C controller runs either in master mode or slave mode, which is determined by `I2C_MS_MODE`. Figure 29.3-1 shows the architecture of a master, while Figure 29.3-2 shows that of a slave. The I2C controller has the following main parts:

*   Transmit and receive memory (TX/RX RAM): store data to be transmitted and data received respectively.
*   Command controller (CMD_Controller): generate (R)START, STOP, WRITE, READ and END commands
```