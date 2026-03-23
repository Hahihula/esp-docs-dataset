

```markdown
## 28.3 I2C Architecture

Figure 28.3-1. I2C Master Architecture

Figure 28.3-2. I2C Slave Architecture

The I2C controller runs either in master mode or slave mode, which is determined by `I2C_MS_MODE`. Figure 28.3-1 shows the architecture of a master, while Figure 28.3-2 shows that of a slave. The I2C controller has the following main parts:

* transmit and receive memory (TX/RX RAM)
* command controller (CMD_Controller)
* SCL clock controller (SCL_FSM)
```