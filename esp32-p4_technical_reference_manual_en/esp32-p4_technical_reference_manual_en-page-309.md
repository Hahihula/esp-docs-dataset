

```markdown
Register 4.77, AXI_DMA_IN_CONF0_CHn_REG (n: 0-2) (0x0010+0x68*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | AXI_DMA_IN_RST_CHn                         | Write 1 and then 0 to reset RX channel n FSM and RX FIFO pointer.(R/W)      |
| 29  | AXI_DMA_IN_LOOP_TEST_CHn                   | Reserved. (R/W)                                                              |
| 28  | AXI_DMA_MEM_TRANS_EN_CHn                   | Configures whether to enable memory-to-memory data transfer.<br>0: Disable<br>1: Enable<br>(R/W) |
| 27  | AXI_DMA_IN_ETM_EN_CHn                      | Configures whether to enable ETM control for RX channel n.<br>0: Disable<br>1: Enable<br>(R/W) |
| 26  | AXI_DMA_IN_BURST_SIZE_SEL_CHn              | Configures the burst length for RX channel n.<br>0: 8 bytes<br>1: 16 bytes<br>2: 32 bytes<br>3: 64 bytes<br>4: 128 bytes<br>5 ~ 7: Invalid<br>(R/W) |
| 25  | AXI_DMA_IN_CMD_DISABLE_CHn                 | Configures whether to disable command on RX channel n.<br>0: Enable<br>1: Disable<br>(R/W) |
| 24  | AXI_DMA_IN_ECC_AEC_EN_CHn                  | Configures whether AXI DMA can access external memory space for ECC and AES via RX channel n.<br>0: Not access<br>1: Access<br>(R/W) |
| 23  | AXI_DMA_INDESCR_BURST_EN_CHn               | Configures whether to enable INCR burst transfer for RX channel n to read descriptors when accessing internal memory.<br>0: Disable<br>1: Enable<br>(R/W) |

```