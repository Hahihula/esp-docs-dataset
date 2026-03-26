

```markdown
## Register 20.85. HP_SYSTEM_ICM_MST_AWQOS_REGO_REG (0x0030)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 0                                                                             |
| 30  | 0                                                                             |
| 29  | 0                                                                             |
| 28  | HP_SYSTEM_ICM_PDMA_INT_AWQOS                                               |
| 27  | 0                                                                             |
| 26  | 0                                                                             |
| 25  | 0                                                                             |
| 24  | HP_SYSTEM_ICM_H264_DMA_M1_AWQOS                                            |
| 23  | 0                                                                             |
| 22  | 0                                                                             |
| 21  | 0                                                                             |
| 20  | HP_SYSTEM_ICM_GDMA_M2_AWQOS                                                |
| 19  | 0                                                                             |
| 18  | 0                                                                             |
| 17  | 0                                                                             |
| 16  | HP_SYSTEM_ICM_DMA2D_AWQOS                                                 |
| 15  | 0                                                                             |
| 14  | 0                                                                             |
| 13  | 0                                                                             |
| 12  | HP_SYSTEM_ICM_CACHE_AWQOS                                                 |
| 11  | 0                                                                             |
| 10  | 0                                                                             |
| 9   | 0                                                                             |
| 8   | HP_SYSTEM_ICM_CPU_AWQOS                                                   |

HP_SYSTEM_ICM_CPU_AWQOS Configures the AWQoS value for the CPU ICM. (R/W)
HP_SYSTEM_ICM_CACHE_AWQOS Configures the AWQoS value for the CACHE. (R/W)
HP_SYSTEM_ICM_DMA2D_AWQOS Configures the AWQoS value for the DMA2D. (R/W)
HP_SYSTEM_ICM_GDMA_M1_AWQOS Configures the AWQoS value for the DW-GDMA MST1. (R/W)
HP_SYSTEM_ICM_GDMA_M2_AWQOS Configures the AWQoS value for the DW-GDMA MST2. (R/W)
HP_SYSTEM_ICM_H264_DMA_M1_AWQOS Configures the AWQoS value for the H264 DMA MST1. (R/W)
HP_SYSTEM_ICM_H264_DMA_M2_AWQOS Configures the AWQoS value for the H264 DMA MST2. (R/W)
HP_SYSTEM_ICM_PDMA_INT_AWQOS Configures the AWQoS value for the AXI GDMA. (R/W)

## Register 20.86. HP_SYSTEM_ICM_DLOCK_TIMEOUT_REG (0x0048)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | 0                                                                             |
| 29  | 0                                                                             |
| 28  | 0                                                                             |
| 27  | 0                                                                             |
| 26  | 0                                                                             |
| 25  | 0                                                                             |
| 24  | 0                                                                             |
| 23  | 0                                                                             |
| 22  | 0                                                                             |
| 21  | 0                                                                             |
| 20  | 0                                                                             |
| 19  | 0                                                                             |
| 18  | 0                                                                             |
| 17  | 0                                                                             |
| 16  | 0                                                                             |
| 15  | 0                                                                             |
| 14  | 0                                                                             |
| 13  | 0                                                                             |
| 12  | 0                                                                             |
| 11  | 0                                                                             |
| 10  | 0                                                                             |
| 9   | 0                                                                             |
| 8   | 0                                                                             |
| 7   | 0                                                                             |
| 6   | 0                                                                             |
| 5   | 0                                                                             |
| 4   | 0                                                                             |
| 3   | 0                                                                             |
| 2   | 0                                                                             |
| 1   | 0                                                                             |
| 0   | 2048                                                                         |

HP_SYSTEM_ICM_DLOCK_TIMEOUT Configures the deadlock timeout threshold value. Deadlock will occur if there is no response within the configured threshold. (R/W)
```