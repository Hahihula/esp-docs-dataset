**Title: Chapter 21 I2C Controller (I2C)**

**Body Text:**
One way many I2C Slave devices are designed is by exposing a register block containing various settings. The I2C Master can write one or more of these registers by sending the Slave a register address. The ESP32 I2C Slave controller has hardware support for such a scheme.

Specifically, on the Slave, `I2C_FIFO_ADDR_CFG_EN` can be set so that the I2C Master can write to a specified register address inside the I2C Slave memory block. Figure 21.3-7 shows the Master writing N-bytes of data byte0 ~ byte(N-1) from the RAM unit to register address M (determined by addrM in RAM unit) with the Slave.

In this mode, Slave can receive up to 32 bytes of valid data. When Master needs to transmit extra amount of data, segmented transmission can be enabled.

**Figure Caption:**
Figure 21.3-7. I2C Master Writes to addrM in RAM of Slave with 7-bit Address

**Table (Master):**
| cmd | op_code | byte_num |
|-----|---------|----------|
| cmd0 | RSTART | -        |
| cmd1 | WRITE   | N+2      |
| cmd2 | STOP    | -        |

**Figure Description:**
The figure shows a block diagram with two sections labeled "Master" and "Slave". The Master section includes commands (cmd) such as RSTART, WRITE, and STOP. There is also an SCL line connecting the master to the slave.

The Slave side has RAM memory blocks showing addresses like addr0, addr1, byte0, etc., up to addr(N+1). It shows how data from the Master's address space (addr(N-1)) can be written into the Slave’s memory block at address M. The SDA line is also depicted.

**Additional Text:**
If the data size exceeds the capacity of a 14-byte read/write cmd, the END command can be called to enable segmented transmission. Figure 21.3-8 shows the Master writing data to the Slave, in three segments. The first segment shows the configuration of the Master’s commands and the preparation of data in the RAM unit.

When the I2CTrans_Start bit is enabled, the Master starts transmission. After executing the END command, the Master will turn off the SCL clock and pull the SCL low to reserve the bus and prevent any other device from transacting on the bus. The controller will generate an I2C_END_DETECT_INT interrupt to notify the software.

**Footer:**
Espressif Systems
395 ESP32 TRM (Version 5.6)
Submit Documentation Feedback