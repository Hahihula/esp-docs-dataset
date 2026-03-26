

```markdown
- If the memory is empty: The read and write pointers remain unchanged (the value of the read pointer equals to the value of the write pointer at this point).
- If the memory is not empty: Increments the read pointer by 1. The write pointer remains unchanged.

Note:
* The incremental operation for the read and write pointers is in a circular manner, i.e., when the value of the read or write pointer reaches the boundary of the memory, the incremental operation resets the value of the pointer to zero.
* Within the LP I2S internal memory architecture, the system always reads the oldest data in the memory.

## 47.9 Interrupts

ESP32-P4's LP I2S can generate the `LP_I2S_INTR` interrupt signal that will be sent to the *Interrupt Matrix*. There are several internal interrupt sources from LP I2S that can generate the above interrupt signals as follows:

* `LP_I2S_RX_HUNG_INT`: Triggered when the data reception is timed out. For example, if the LP I2S module is configured as RX slave mode, but the master does not transmit data for a long time (specified in `LP_I2S_LC_HUNG_CONF_REG`), this interrupt will be triggered.
* `LP_I2S_RX_DONE_INT`: Triggered when the data reception is completed.
* `LP_I2S_RX_FIFOMEM_UDF_INT`: Triggered when the LP I2S memory is read empty.
* `LP_I2S_RX_MEM_THRESHOLD_INT`: Triggered when the data in LP I2S memory is larger than the value configured in `LP_I2S_RX_MEM_THRESHOLD`.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 *Interrupt Matrix* > Section 12.2 *Interrupt Terminology in ESP32-P4*.

Each interrupt source can be configured by a common set of registers that are described in Section *Interrupt Configuration Registers*. The specific registers can be found in Section 47.10 *Register Summary*.
```