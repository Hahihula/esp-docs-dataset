

```markdown
- Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2C_master continues data transfer.
- Not match: If the received ACK value does not match ack_exp, I2C_master generates an I2C_NACK_INT (master) interrupt and stops data transfer.

12. I2C_slave receives memory address sent by I2C_master and adds the offset.
13. I2C_master sends a RSTART and the third byte in TX RAM, which is ((0x78 | I2C_SLAVE_ADDR[6:0])«1)and an R bit.
14. I2C_slave repeats step 11. If its address matches the address sent by I2C_master, I2C_slave proceed on to the next steps.
15. Write data to be sent to TX RAM of I2C_slave in non-FIFO mode.
16. I2C_slave sends data, and I2C_master checks ACK value or not according to ack_check_en (master) in the READ command.
17. After I2C_master has received the last byte of data, set ack_value (master) to 1. I2C_slave will stop transfer once receiving the I2C_NACK_INT interrupt.
18. After data transfer completes, I2C_master executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

44.6.8 I2C_master Reads I2C_slave with a 7-bit Address in Multiple Command Sequences
```