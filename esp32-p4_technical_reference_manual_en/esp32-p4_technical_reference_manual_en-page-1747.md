

```markdown
| Bit Field | Description |
|-----------|-------------|
| 31        | (reserved) |
| 6         | CSI_BRIG_DMA_CFG_HAS_UPDATED_INT_ST |
| 5         | CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT_ST |
| 4         | CSI_BRIG_CSI_BUF_OVERUN_INT_ST |
| 3         | CSI_BRIG_VADR_NUM_GT_INT_ST |
| 2         | CSI_BRIG_VADR_NUM_LT_INT_ST |
| 1         | CSI_BRIG_DISCARD_INT_ST |
| 0         | Reset |

CSI_BRIG_VADR_NUM_GT_INT_ST The masked interrupt status of CSI_BRIG_VADR_NUM_GT_INT. (RO)

CSI_BRIG_VADR_NUM_LT_INT_ST The masked interrupt status of CSI_BRIG_VADR_NUM_LT_INT. (RO)

CSI_BRIG_DISCARD_INT_ST The masked interrupt status of CSI_BRIG_DISCARD_INT. (RO)

CSI_BRIG_CSI_BUF_OVERUN_INT_ST The masked interrupt status of CSI_BRIG_CSI_BUF_OVERUN_INT. (RO)

CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT_ST The masked interrupt status of CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT. (RO)

CSI_BRIG_DMA_CFG_HAS_UPDATED_INT_ST The masked interrupt status of CSI_BRIG_DMA_CFG_HAS_UPDATED_INT. (RO)
```