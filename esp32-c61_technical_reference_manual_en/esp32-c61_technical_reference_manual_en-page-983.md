

```markdown
## 27.6.4 I2Cmaster Writes to I2Cslave with a 7-bit Address in Multiple Command Sequences

### 27.6.4.1 Introduction

Figure 27.6-4. I2Cmaster Writing to I2Cslave with a 7-bit Address in Multiple Sequences
```

```markdown
Given that the I2C Controller RAM holds only the size of TX/RX FIFO depth, when data are too large to be processed, it is advised to transmit them in multiple command sequences. Each command sequence ends with an END command. When the controller executes this END command, SCL will be pulled low, and the software can refresh command sequence registers and the RAM for the next transfer.

Figure 27.6-4 shows how I2Cmaster writes to an I2C slave in two or three segments as an example. For the first segment, the CMD_Controller registers are configured as shown in Segment0. Once data in I2Cmaster’s RAM is ready and I2C_TRANS_START is set, I2Cmaster initiates data transfer. After executing the END command, I2Cmaster turns off the SCL clock and pulls SCL low to reserve the bus. Meanwhile, the controller generates an I2C_END_DETECT_INT interrupt.

For the second segment, after detecting the I2C_END_DETECT_INT interrupt, the software refreshes the
```