

```markdown
Chapter 5  VDMA Controller (VDMA)
GoBack

Register 5.11. DMAC_CHn_CTLO_REG (n: 1-4) (0x0100*n + 0x0018)

Continued from the previous page...

DMAC_CHn_NONPOSTED_LASTWRITE_EN Configures whether to enable non-posted writes throughout the block transfer.
Posted writes refers to sending data without the need to write the data into the destination (the data may still be in transit); VDMA can consider this write request to be complete. Non-posted writes refers to sending data that needs to be written into the destination and requires a response, only then can VDMA consider this write request to be complete.
0: Posted writes can be used throughout the block transfer.
1: Posted writes can be used at the end of the block transfer (within the block). The last write must be non-posted to ensure synchronization between the generation of the block completion interrupt and the final written data reaching the destination.

(R/W)
```