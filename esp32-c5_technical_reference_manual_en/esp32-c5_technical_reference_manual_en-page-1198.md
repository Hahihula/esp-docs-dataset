

```markdown
- Dual address mode, which uses slave address and slave memory or register address
```

## 34.3 Architecture Overview

Figure 34.3-1. I2C Master Architecture

Figure 34.3-2. I2C Slave Architecture

The I2C controller runs either in master mode or slave mode, which is determined by `I2C_MS_MODE`. Figure 34.3-1 shows the architecture of a master, while Figure 34.3-2 shows that of a slave. The I2C controller has the following main parts:

* Transmit and receive memory (TX/RX RAM): stores data to be transmitted and data received respectively.
```