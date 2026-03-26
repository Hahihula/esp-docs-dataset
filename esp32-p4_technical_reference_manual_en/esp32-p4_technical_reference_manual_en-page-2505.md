

# 47.11 Registers

The addresses in this section are relative to LP I2S base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 471. LP_I2S_RX_MEM_CONF_REG (0x0008)

```
31                 17   16                9    8
+-----------------------------+---------------+
|         (reserved)          | LP_I2S_RX_MEM_THRESHOLD | LP_I2S_RX_MEM_FIFO_CNT |
+-----------------------------+---------------+
|       0x0                   |               Reset        |
+-----------------------------+---------------+
```

LP_I2S_RX_MEM_FIFO_CNT Configures the number of data in the RX memory. (RO)

LP_I2S_RX_MEM_THRESHOLD Configures the RX memory threshold. LP I2S RX memory triggers an interrupt when the data in the memory exceeds (not including equals) this threshold. (R/W)