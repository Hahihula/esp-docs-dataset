

```markdown
Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 9 Interrupt Matrix > Section 9.2 Interrupt Terminology in ESP32-C61.
```

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 27.7.1 I2C Register Summary.

## 27.6 Programming Procedures

This section provides programming examples for typical communication scenarios. For the convenience of description, I2C masters and slaves in all subsequent figures are ESP32-C61 I2C controller. I2C master is referred to as I2Cmaster, and I2C slave is referred to as I2Cslave.

### 27.6.1 I2Cmaster Writes to I2Cslave with a 7-bit Address in One Command Sequence

#### 27.6.1.1 Introduction

![Figure 27.6-1. I2Cmaster Writing to I2Cslave with a 7-bit Address](image_reference)

Figure 27.6-1 shows how I2Cmaster writes N bytes of data to I2Cslave registers or RAM using 7-bit addressing. As shown in Figure 27.6-1, the first byte in the RAM of I2Cmaster is a 7-bit I2Cslave address followed by a R/W bit. When the R/W bit is 0, it indicates a WRITE operation. The remaining bytes are used to store data ready for transfer. The cmd box contains related command sequences.

After the command sequence is configured and data in RAM is ready, I2Cmaster enables the controller and initiates data transfer by setting the I2C_TRANS_START bit. The controller has four steps to take:

1. Wait for SCL to go high, to avoid SCL being used by other masters or slaves.
2. Execute a RSTART command by sending a START bit.
```