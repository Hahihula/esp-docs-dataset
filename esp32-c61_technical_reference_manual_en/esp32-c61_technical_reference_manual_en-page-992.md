

```markdown
## 27.6.8 I2Cmaster Reads I2Cslave with a 7-bit Address in Multiple Command Sequences

### 27.6.8.1 Introduction

Figure 27.6-8 shows how I2Cmaster reads (N+M) bytes of data from an I2C slave in two/three segments separated by END commands. Configuration procedures are described as follows:

1. The procedures for Segment0 is similar to 27.6-5, except that the last command is an END.
2. Prepare data in the TX RAM of I2Cslave, and set I2C_TRANS_START to start data transfer. After executing the END command, I2Cmaster refreshes command registers and the RAM as shown in Segment1, and clears the corresponding I2C_END_DETECT_INT interrupt. If cmd2 in Segment1 is a STOP, then data is
```