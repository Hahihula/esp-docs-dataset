

```markdown
Chapter 19 Permission Control (PMS)

Register 19.39. PMS_DMA_SDMMC_PMS_R_REG (0x01BC)
```

| 31 | oxffffffff | Reset |
|----|-------------|-------|

**PMS_DMA_SDMMC_R_PMS** Configures read permission for SDMMC to access 32 address ranges.

Bit 0 corresponds to region0, and so on.

- O: Disable read permission.
- 1: Enable read permission.

(R/W)

Register 19.40. PMS_DMA_SDMMC_PMS_W_REG (0x01C0)
```

| 31 | oxffffffff | Reset |
|----|-------------|-------|

**PMS_DMA_SDMMC_W_PMS** Configures write permission for SDMMC to access 32 address ranges. Bit 0 corresponds to region0, and so on.

- O: Disable write permission.
- 1: Enable write permission.

(R/W)
```