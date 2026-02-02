**Title: Chapter 21 I2C Controller (I2C)**

---

### Figure Caption:
- **Figure 21.3-10:** Master Reads from Slave with 10-bit Address

---

#### Body Text:

Figure 21.3-11 shows the Master reading data from a specified address in the Slave. This mode can be enabled by setting I2C_FIFO_ADDR_CFG_EN and preparing the data to be read by the master in the Slave RAM block.

Subsequently, the address of the Slave and the address of the specified register (that is, M) have to be determined by the master. Finally, the I2CTrans_start bit must be set in the Master to initiate the read operation, following which the Slave will fetch N bytes of data from RAM and send them to the Master.

---

### Figure Caption:
- **Figure 21.3-11:** Master Reads N Bytes of Data from addrM in Slave with 7-bit Address

---

#### Body Text:

Figure 21.3-12 shows the Master reading N+M bytes of data in three segments from the Slave.

The first segment shows the configuration of the cmd and the preparation of data in the Slave RAM.
When the I2CTrans_start bit is enabled, the Master starts the operation. The Master will refresh the cmd after executing the END command. It will clear the I2C_endDetect_int interrupt, set the I2C_trans_start bit
and resume the transaction.

To stop the transaction,
the Master will configure the cmd as follows:
- After detecting the I2C_endDetect_int interrupt.
- After setting the I2C_trans_start bit,

Master will send a STOP bit to stop the transaction. 

---

**Footer:**
- Espressif Systems
- ESP32 TRM (Version 5.6)
- Page number: 398

**Action Links:** 
- Submit Documentation Feedback