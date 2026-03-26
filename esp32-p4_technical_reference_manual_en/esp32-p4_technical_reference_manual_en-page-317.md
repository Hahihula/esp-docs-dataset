

```markdown
Register 4.89. AXI_DMA_OUT_CONFO_CHn_REG(n: 0-2) (0x0148+0x68*n)

Continued from the previous page...

AXI_DMA_OUT_ECC_AEC_EN_CHn Configures whether AXI DMA can access external memory space for ECC and AES via TX channel n.
O: Not access
1: Access
(R/W)

AXI_DMA_OUTDSCR_BURST_EN_CHn Configures whether to enable INCR burst transfer for TX channel n reading descriptors when accessing internal memory.
O: Disable
1: Enable
(R/W)

Register 4.90. AXI_DMA_OUT_CONF1_CHn_REG (n: 0-2) (0x014C+0x68*n)
```

```markdown
AXI_DMA_OUT_CHECK_OWNER_CHn Configures whether to enable owner bit check for TX channel n.
O: Disable
1: Enable
(R/W)
```