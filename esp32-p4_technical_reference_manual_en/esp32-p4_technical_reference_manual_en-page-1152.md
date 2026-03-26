

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| PMS_DMA_AHB_PDMA_DUMMY_W_PMS_REG           | GDMA-AHB Dummy write permission control register                          | 0x0218    | R/W    |
| PMS_DMA_AXI_PDMA_DUMMY_R_PMS_REG           | GDMA-AXI Dummy read permission control register                            | 0x021C    | R/W    |
| PMS_DMA_AXI_PDMA_DUMMY_W_PMS_REG           | GDMA-AXI Dummy write permission control register                           | 0x0220    | R/W    |

### 19.6.2 HP_PERI_PMS_REG

The addresses in this section are relative to the HP_PERI_PMS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column `Access` are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Version Control Registers                 |                                                                             |           |        |
| PMS_HP_PERI_PMS_DATE_REG                  | Version control register                                                    | 0x0000    | R/W    |
| Clock Gating Registers                    |                                                                             |           |        |
| PMS_HP_PERI_PMS_CLK_EN_REG                | Clock gating register                                                      | 0x0004    | R/W    |
| HP CPU Permission Control Registers       |                                                                             |           |        |
| PMS_COREO_MM_HP_PERI_PMS_REGO_REG         | Permission control register 0 for HP CPUO in machine mode                  | 0x0008    | R/W    |
| PMS_COREO_MM_HP_PERI_PMS_REG1_REG         | Permission control register 1 for HP CPUO in machine mode                  | 0x000C    | R/W    |
| PMS_COREO_MM_HP_PERI_PMS_REG2_REG         | Permission control register 2 for HP CPUO in machine mode                  | 0x0010    | R/W    |
| PMS_COREO_MM_HP_PERI_PMS_REG3_REG         | Permission control register 3 for HP CPUO in machine mode                  | 0x0014    | R/W    |
| PMS_COREO_UM_HP_PERI_PMS_REGO_REG         | Permission control register 0 for HP CPUO in user mode                     | 0x0018    | R/W    |
| PMS_COREO_UM_HP_PERI_PMS_REG1_REG         | Permission control register 1 for HP CPUO in user mode                     | 0x001C    | R/W    |
| PMS_COREO_UM_HP_PERI_PMS_REG2_REG         | Permission control register 2 for HP CPUO in user mode                     | 0x0020    | R/W    |
| PMS_COREO_UM_HP_PERI_PMS_REG3_REG         | Permission control register 3 for HP CPUO in user mode                     | 0x0024    | R/W    |
| PMS_CORE1_MM_HP_PERI_PMS_REGO_REG         | Permission control register 0 for HP CPU1 in machine mode                  | 0x0028    | R/W    |
| PMS_CORE1_MM_HP_PERI_PMS_REG1_REG         | Permission control register 1 for HP CPU1 in machine mode                  | 0x002C    | R/W    |
| PMS_CORE1_MM_HP_PERI_PMS_REG2_REG         | Permission control register 2 for HP CPU1 in machine mode                  | 0x0030    | R/W    |
```