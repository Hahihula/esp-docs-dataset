

```markdown
Register 19.4. PMS_DMA_REGIONn_HIGH_REG (n: 0-31) (0x000C+0x8*n)

PMS_DMA_REGIONn_HIGH   Configures the high 20 bits of the end address for regionn. (R/W)

Register 19.5. PMS_DMA_GDMA_CHn_R_PMS_REG (n: 0-3) (0x0108+0x8*n)

PMS_DMA_GDMA_CHn_R_PMS   Configures the permission for GDMA chn to read 32 address regions. Bit 0 corresponds to region0, and so on.
    0: Disable read permission.
    1: Enable read permission.
(R/W)

Register 19.6. PMS_DMA_GDMA_CHn_W_PMS_REG (n: 0-3) (0x010C+0x8*n)

PMS_DMA_GDMA_CHn_W_PMS   Configures the permission for GDMA chn to write 32 address regions. Bit 0 corresponds to region0, and so on.
    0: Disable write permission.
    1: Enable write permission.
(R/W)
```