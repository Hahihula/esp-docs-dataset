**Chapter 5: eFuse Controller**

---

### Updating eFuse read registers

The eFuse Controller reads internal eFuses to update corresponding registers. This read operation happens on system reset and can also be triggered manually by users as needed (e.g., if new eFuse values have been programmed). The process of triggering a read operation by users is as follows:

1. Configure the field `EFUSE_OP_CODE` in register `EFUSE_CONF_REG` to 0x5AA5.
2. Configure the field `EFUSE_READ_CMD` in register `EFUSE_CMD_REG` to 1.
3. Poll register `EFUSE_CMD_REG` until it is 0x0, or wait for a READ_DONE interrupt. Information on how to identify a READ_DONE interrupt is provided below in this section.

4. Users read the values of each parameter from memory.

The eFuse read registers will hold all values until the next read operation.

---

### Error detection

Error record registers allow users to detect if there are any inconsistencies in the stored backup eFuse parameters.
- Registers `EFUSE_RD_REPEAT_ERRR ~ 3_REG` indicate if there are any errors of programmed parameters (except for `EFUSE_WR_DIS`) in BLOCK0 (value 1 indicates an error is detected, and the bit becomes invalid; value 0 indicates no error).
- Registers `EFUSE_RD_RS_ERROR ~ 1_REG` store the number of corrected bytes as well as the result of RS decoding during eFuse reading `BLOCK1 ~ BLOCK10`.

The values of above registers will be updated every time after the eFuse read registers have been updated.

---

### Identifying the completion of a program/read operation

The methods to identify the completion of a program/read operation are described below. Please note that bit 1 corresponds to a program operation, and bit 0 corresponds to a read operation.
- **Method one:**
  - Poll bit I/O in register `EFUSE_INT_RAW_REG` until it becomes 1, which represents the completion of a program/read operation.

- **Method two:**
  - Set bit I/O in register `EFUSE_INT_ENA_REG` to 1 to enable the eFuse Controller to post a PGM_DONE or READ_DONE interrupt.
  - Configure the Interrupt Matrix to enable the CPU to respond to eFuse interrupt signals, see Chapter 9 Interrupt Matrix (INTERRUPT).
  - Wait for the PGM/READDone interrupt.
  - Set bit I/O in register `EFUSE_INT_CLR_REG` to 1 to clear the PGM/READ_DONE interrupt.

---

### Note

When eFuse controller updating its registers, it will use `EFUSE_PGM_DATA[0..7]` again to store data. So please do not write important data into these registers before this updating process initiated.
- **Espressif Systems**
- Page 421
- Submit Documentation Feedback