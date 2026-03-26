

```markdown
Register 4.104. AXI_DMA_IN_MEM_CONF_REG (0x0278)
```

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 6   | `AXI_DMA_OUT_MEM_FORCE_PD`          | Configures whether to force power down memory for TX.                        |
| 5   | `AXI_DMA_OUT_MEM_FORCE_PU`          | Configures whether to force power up memory for TX.                          |
| 4   | `AXI_DMA_OUT_MEM_CLK_FORCE_EN`      | Configures memory clock gating for TX.                                      |
| 3   | (reserved)                          |                                                                             |
| 2   | `AXI_DMA_IN_MEM_FORCE_PD`           | Configures whether to force power down memory for RX.                        |
| 1   | `AXI_DMA_IN_MEM_FORCE_PU`           | Configures whether to force power up memory for RX.                          |
| 0   | `AXI_DMA_IN_MEM_CLK_FORCE_EN`       | Configures memory clock gating for RX.                                      |

---

**AXI_DMA_IN_MEM_CLK_FORCE_EN**  
Configures memory clock gating for RX.  
- 0: Support clock only when AXI DMA accesses memory  
- 1: Always force the clock on (R/W)

---

**AXI_DMA_IN_MEM_FORCE_PU**  
Configures whether to force power up memory for RX.  
- 0: Not force power up  
- 1: Force power up (R/W)

---

**AXI_DMA_IN_MEM_FORCE_PD**  
Configures whether to force power down memory for RX.  
- 0: Not force power down  
- 1: Force power down (R/W)

---

**AXI_DMA_OUT_MEM_CLK_FORCE_EN**  
Configures memory clock gating for TX.  
- 0: Support clock only when AXI DMA accesses memory  
- 1: Always force the clock on (R/W)

---

**AXI_DMA_OUT_MEM_FORCE_PU**  
Configures whether to force power up memory for TX.  
- 0: Not force power up  
- 1: Force power up (R/W)

---

**AXI_DMA_OUT_MEM_FORCE_PD**  
Configures whether to force power down memory for TX.  
- 0: Not force power down  
- 1: Force power down (R/W)
```