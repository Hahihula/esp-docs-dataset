

```markdown
## 29.6 Programming Example

This sections provides programming examples for typical communication scenarios. ESP32-C6 has two I2C controllers. For the convenience of description, I2C masters and slaves in all subsequent figures are ESP32-C6 I2C controllers. I2C master is referred to as `I2C_master`, and I2C slave is referred to as `I2C_slave`.

### 29.6.1 I2C_master Writes to I2C_slave with a 7-bit Address in One Command Sequence

#### 29.6.1.1 Introduction

Figure 29.6-1 shows how `I2C_master` writes N bytes of data to `I2C_slave` registers or RAM using 7-bit addressing. As shown in figure 29.6-1, the first byte in the RAM of `I2C_master` is a 7-bit `I2C_slave` address followed by a R/W bit. When the R/W bit is 0, it indicates a WRITE operation. The remaining bytes are used to store data ready for transfer. The cmd box contains related command sequences.

After the command sequence is configured and data in RAM is ready, `I2C_master` enables the controller and initiates data transfer by setting the `I2C_TRANS_START` bit. The controller has four steps to take:

1. Wait for SCL to go high, to avoid SCL being used by other masters or slaves.
2. Execute a RSTART command by sending a START bit.
3. Execute a WRITE command by taking N+1 bytes from the RAM in order and send them to `I2C_slave` in the same order. The first byte is the address of `I2C_slave`.
4. Execute a STOP command. Once the `I2C_master` transfers a STOP bit, an `I2C_TRANS_COMPLETE_INT` interrupt is generated.
```