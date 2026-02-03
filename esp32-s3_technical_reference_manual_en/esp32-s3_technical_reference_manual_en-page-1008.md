**Title: Chapter 27 I2C Controller (I2C)**

---

### Table of Commands and Their Functions:

| Command | Master/Slave | Description |
|---------|--------------|-------------|
| I2C_COMMAND0 | master | START |
| I2C_COMMAND1 | master | WRITE |
| I2C_COMMAND2 | master | START |
| I2C_COMMAND3 | master | WRITE |
| I2C_COMMAND4 | master | READ |
| I2C_COMMAND5 | master | READ |
| I2C_COMMAND6 | master | STOP |

---

### Instructions:

1. **Configure I2C_SLAVE_ADDRESS (slave) in I2C_SLAVE_ADDRESS'REG (slave):** Set slave's 10-bit address, and set `I2C_ADDR_10BIT_EN` to enable 10-bit addressing.

2. **Write the Address of I2C_slave:**
   - The first byte comprises `(0x78 | I2C_SLAVE_ADDRESS[9:8])<1>` followed by a `R/W` bit, which is 1 and indicates a WRITE operation.
   - The second byte address is `I2C_SLAVE_ADDRESS[7:0]`.
   - The third byte is `(0x78 | I2C_SLAVE_ADDR[9:8])<1>`, indicating a READ operation.

3. **Write to I2C_CONF_UPGRADE (master) and I2C_CONF_UPGRADE (slave):** Synchronize registers by writing `I2C TRANS_START` command from master's transfer.
   - Start the slave’s transfer according to Section 27.4.14, where:
     - Master checks ACK value against its own address in `I2C_SLAVE_ADDRESS`.
     - When `ack_check_en` is set and `master` writes a byte: If `ack_check_en` matches master's default.
       - Matched values continue data transfer; mismatch generates an `I2C_NACK_INT`.

4. **Send RSTART:** Send the third byte in TX RAM, which includes `(0x78 | I2C_SLAVE_ADDRESS[9:8])<1>` and a `R/W` bit indicating READ.

5. **Repeat Steps 1-3 for subsequent operations if address matches `I2C_master`'s transfer command; proceed to next steps**:

6. After generating the `I2C.Stretch_INT`, set `I2C.Stretch_Cause` as follows:
   - If slave's address is matched, send data.
   - Write data in either FIFO or non-FIFO mode according to Section 27.4.10.

7. **Release SCL:** Set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to release SCL after operations are completed:

---

**Footer:**
- Espresso Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback