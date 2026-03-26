

```markdown
## 44.6.8.1 Introduction

Figure 44.6-8. I2Cmaster Reading I2Cslave with a 7-bit Address in Segments

Segment0

Master:
cmd cmd0 op_code RSTART byte_num
cmd1 WRITE 1
cmd2 READ N
cmd3 END

RAM addr0 (slave_addr<<1 r/w) byte0
addr1 byte1
addr2 byte2
...
addr(N-1) byte(N-1)

Slave:
RAM addr0 byte0
addr1 byte1
addr2 ...
addr(N-1) byte(N-1)

Segment1

Master:
cmd cmd0 op_code READ M-1
cmd1 READ 1
cmd2 END/STOP

RAM addrN byteN
addr(N+1) byte(N+1)
addr(N+2) byte(N+2)
...
addr(M+N-1) byte(M+N-1)

Slave:
RAM addr(N-1) Byte(N-1)
addrN byteN
addr2 ...
addr(M+N-1) byte(M+N-1)

Segment2

Master:
cmd cmd0 op_code STOP M-1
```

Figure 44.6-8 shows how I2Cmaster reads (N+M) bytes of data from an I2C slave in two/three segments separated by END commands. Configuration procedures are described as follows:

1. The procedures for Segment0 is similar to 44.6-5, except that the last command is an END.
2. Prepare data in the TX RAM of I2Cslave, and set I2C_TRANS_START to start data transfer. After executing the END command, I2Cmaster refreshes command registers and the RAM as shown in Segment1, and clears the corresponding I2C_END_DETECT_INT interrupt. If cmd2 in Segment1 is a STOP, then data is read from I2Cslave in two segments. I2Cmaster resumes data transfer by setting I2C_TRANS_START and terminates the transfer by sending a STOP bit.
3. If cmd2 in Segment1 is an END, then data is read from I2Cslave in three segments. After the second data
```