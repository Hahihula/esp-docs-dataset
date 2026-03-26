

```markdown
## Register 5.7. DMAC_LOWPOWER_CFG1_REG (0x0064)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)         |                                                                             |
| 24  |                    |                                                                             |
| 23  |                    |                                                                             |
| 22  |                    |                                                                             |
| 21  |                    |                                                                             |
| 20  |                    |                                                                             |
| 19  |                    |                                                                             |
| 18  |                    |                                                                             |
| 17  | DMAC_MXIF_LPDLY    | Configures the value of the global low-power delay counter and the DMA channel low-power delay counter. The programmed value must be greater than or equal to 0x4. If it is less than 0x4, the field will reset to 0x40. (R/W) |
| 16  | DMAC_SBIU_LPDLY    | Configures the value of the SBIU low-power delay counter. The programmed value must be greater than or equal to 0x4. If it is less than 0x4, the field will reset to 0x40. (R/W) |
| 15  | DMAC_GLCH_LPDLY    | Configures the value of the AXI master interface low-power delay counter. The programmed value must be greater than or equal to 0x4. If it is less than 0x4, the field will reset to 0x40. (R/W) |
| 8   |                    |                                                                             |
| 7   |                    |                                                                             |
| 6   |                    |                                                                             |
| 5   |                    |                                                                             |
| 4   |                    |                                                                             |
| 3   |                    |                                                                             |
| 2   |                    |                                                                             |
| 1   |                    |                                                                             |
| 0   | Reset              | 0x40                                                                          |

## Register 5.8. DMAC_CHn_SARO_REG (n: 1-4) (0x0100*n)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  |                    |                                                                             |
| ... | DMAC_CHn_SARO      | Configures the source address of DMA transfer. This field is updated after each source transfer. DMAC_CHn_SINC determines whether the address increments or remains unchanged on every source transfer throughout the block transfer. (R/W) |

## Register 5.9. DMAC_CHn_DARO_REG (n: 1-4) (0x0100*n + 0x0008)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  |                    |                                                                             |
| ... | DMAC_CHn_DARO      | Configures the destination address of DMA transfer. This field is updated after each source transfer. DMAC_CHn_DINC determines whether the address increments or remains unchanged on every destination transfer throughout the block transfer. (R/W) |
```