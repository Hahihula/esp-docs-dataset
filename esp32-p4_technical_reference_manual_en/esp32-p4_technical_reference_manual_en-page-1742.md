

```markdown
## Register 36.147. CSI_BRIG_DMA_REQ_CFG_REG (0x0008)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 28  |                                | (reserved)                                                                  |
| 27  |                                | (reserved)                                                                  |
| 26  |                                | (reserved)                                                                  |
| 25  |                                | (reserved)                                                                  |
| 24  |                                | (reserved)                                                                  |
| 23  |                                | (reserved)                                                                  |
| 22  |                                | (reserved)                                                                  |
| 21  |                                | (reserved)                                                                  |
| 20  |                                | (reserved)                                                                  |
| 19  |                                | (reserved)                                                                  |
| 18  |                                | (reserved)                                                                  |
| 17  | CSI_BRIG_CSI_DMA_FLOW_CONTROLLER | Configures the DMA flow controller.                                        |
| 16  |                                | (reserved)                                                                  |
| 15  |                                | (reserved)                                                                  |
| 14  |                                | (reserved)                                                                  |
| 13  |                                | (reserved)                                                                  |
| 12  | CSI_BRIG_DMA_CFG_UPD_BY_BLK    | Configures when `CSI_BRIG_DMA_BURST_LEN` and `CSI_BRIG_DMABLK_SIZE` are updated. |
| 11  |                                 | 0: Update upon completion of each VDMA block transfer                       |
|     |                                 | 1: Update at the end of each frame transfer (R/W)                           |
| 10  |                                | (reserved)                                                                  |
| 9   |                                | (reserved)                                                                  |
| 8   |                                | (reserved)                                                                  |
| 7   |                                | (reserved)                                                                  |
| 6   |                                | (reserved)                                                                  |
| 5   |                                | (reserved)                                                                  |
| 4   |                                | (reserved)                                                                  |
| 3   |                                | (reserved)                                                                  |
| 2   |                                | (reserved)                                                                  |
| 1   |                                | (reserved)                                                                  |
| 0   | CSI_BRIG_DMA_BURST_LEN         | Configures the amount of 64-bit data in a VDMA burst transfer. (R/W)        |

### Description:
- **CSI_BRIG_DMA_CFG_UPD_BY_BLK**: Determines when `CSI_BRIG_DMA_BURST_LEN` and `CSI_BRIG_DMABLK_SIZE` are updated.
    - `0`: Updated upon completion of each VDMA block transfer.
    - `1`: Updated at the end of each frame transfer. (R/W)
- **CSI_BRIG_CSI_DMA_FLOW_CONTROLLER**: Configures the DMA flow controller.
    - `0`: DMA acts as the flow controller.
    - `1`: CSI_bridge acts as the flow controller. (R/W)

## Register 36.148. CSI_BRIG_DMA_REQ_INTERVAL_REG (0x002C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 28  |                                | (reserved)                                                                  |
| 27  |                                | (reserved)                                                                  |
| 26  |                                | (reserved)                                                                  |
| 25  |                                | (reserved)                                                                  |
| 24  |                                | (reserved)                                                                  |
| 23  |                                | (reserved)                                                                  |
| 22  |                                | (reserved)                                                                  |
| 21  |                                | (reserved)                                                                  |
| 20  |                                | (reserved)                                                                  |
| 19  |                                | (reserved)                                                                  |
| 18  |                                | (reserved)                                                                  |
| 17  |                                | (reserved)                                                                  |
| 16  |                                | (reserved)                                                                  |
| 15  | CSI_BRIG_DMA_REQ_INTERVAL      | Configures the interval of VDMA requests. `16'b1`: 1 clock cycle,           |
|     |                                 | `16'b11`: 2 clock cycles, `16'hFFF`: 16 clock cycles, etc. (R/W)            |

### Description:
- **CSI_BRIG_DMA_REQ_INTERVAL**: Configures the interval of VDMA requests.
    - `16'b1`: 1 clock cycle
    - `16'b11`: 2 clock cycles
    - `16'hFFF`: 16 clock cycles, etc. (R/W)
```