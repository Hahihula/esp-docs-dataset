

```markdown
Chapter 44 I2C Controller (I2C) GoBack


## 44.3 I2C Architecture

Figure 44.3-1. I2C Master Architecture

APB_CLK domain
I2C_SCLK domain

cmd0
cmd1
...
cmd7
cmd_content

cmd_rd
cmd_done

CMD_Controller

I2C_TRANS_START

APB_CLK domain

32x8bits
TX RAM
RX RAM

APB BUS

SCL_LOW_PERIOD
SCL_HIGH_PERIOD
SCL_WAIT_HIGH_PERIOD

SCL_FS M
SCL_MAIN_FS M

Start_Detect
Stop_Detect

DATA_Shifter

I2C_RX_LSB_FIRST
I2C_TX_LSB_FIRST

ack_deal

I2C_SCL_FILTER_EN
0 1 SCL

I2C_SCL_FILTER_THRES
I2C_SAMPLE_SCL_LEVEL

SDA_Filter

I2C_SDA_FILTER_THRES
I2C_SDA_FILTER_EN

0 1 SDA


Figure 44.3-2. I2C Slave Architecture

APB_CLK domain

32x8bits
TX RAM
RX RAM

APB BUS

SCL_FS M
SCL_MAIN_FS M

Start_Detect
Stop_Detect

DATA_Shifter

I2C_RX_LSB_FIRST
I2C_TX_LSB_FIRST

ack_deal

I2C_SCL_FILTER_EN
0 1 SCL

I2C_SCL_FILTER_THRES
I2C_SAMPLE_SCL_LEVEL

SDA_Filter

I2C_SDA_FILTER_THRES
I2C_SDA_FILTER_EN

0 1 SDA


The I2C controller runs either in master mode or slave mode, which is determined by `I2C_MS_MODE`. Figure 44.3-1 shows the architecture of a master, while Figure 44.3-2 shows that of a slave. The I2C controller has the following main parts:

* Transmit and receive memory (TX/RX RAM): store data to be transmitted and data received respectively.
* Command controller (CMD_Controller): generate (R)START, STOP, WRITE, READ, and END commands
```