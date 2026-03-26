

```markdown
1. Software writes 1 to `DMAC_CHn_SUSP`.
2. VDMA halts all transfers from the source, after completing all AXI transfers initiated from the source.
3. VDMA sets `DMAC_CHn_CH_SRC_SUSPENDED_INT` to 1 to indicate that source transfer is suspended.
4. VDMA transfers all the data in channel FIFO to the destination. If `DMAC_CHn_SRC_TR_WIDTH < DMAC_CHn_DST_TR_WIDTH` and `DMAC_CHn_SUSP` is 1, there may still be data in the channel FIFO, but not enough to form a single transfer of `DMAC_CHn_DST_TR_WIDTH`. The remaining data in the channel FIFO will be transferred to the destination if the channel is resumed.
5. VDMA sets `DMAC_CHn_CH_SUSPENDED_INT` to 1 to indicate that the channel is suspended.

After a channel suspend, software can resume the channel by setting `DMAC_CHn_SUSP` to 0. Then, VDMA resumes the DMA transfer from the point where it was suspended.
```

## 5.5.7 Channel Disable

Under normal operation, software enables a channel by writing 1 to `DMAC_CHn_EN`, and VDMA clears `DMAC_CHn_EN` after channel transfer completion. Software can disable a channel before a transfer completes.

### 5.5.7.1 Disabling a Suspended Channel Before Transfer Completion

To disable a suspended channel before transfer completion:

- Write 0 to `DMAC_CHn_EN` after `DMAC_CHn_CH_SUSPENDED_INTSTAT` is set to 1. If `DMAC_CHn_SRC_TR_WIDTH < DMAC_CHn_DST_TR_WIDTH` and `DMAC_CHn_SUSP` is 1, there may still be data in the channel FIFO, but not enough to form a single transfer of `DMAC_CHn_DST_TR_WIDTH`. In this case, once the channel is disabled, the remaining data in the channel FIFO is not transferred to the destination peripheral and is lost.
- VDMA sets `DMAC_CHn_CH_DISABLED_INTSTAT` to 1 to indicate that the channel is disabled and generates an interrupt.

### 5.5.7.2 Disabling a Non-suspended Channel Before Transfer Completion

To disable a non-suspended channel before transfer completion:

- Software writes 0 to `DMAC_CHn_EN` during DMA transfer.
- VDMA halts all transfers from the source, after completing all AXI transfers initiated on the source.
- VDMA transfers all the data in the channel FIFO to the destination. When `DMAC_CHn_SRC_TR_WIDTH < DMAC_CHn_DST_TR_WIDTH` and `DMAC_CHn_EN` is 0, there may still be data in the channel FIFO, but not enough to form a single transfer of `DMAC_CHn_DST_TR_WIDTH`. In this scenario, once the channel is disabled, the remaining data in the channel FIFO is not transferred to the destination peripheral and is lost.
- VDMA sets `DMAC_CHn_CH_DISABLED_INTSTAT` to 1 to indicate that the channel is disabled and generates an interrupt.

**Note:**
```