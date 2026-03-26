

```markdown
Chapter 19 Permission Control (PMS)

Register 19.43. PMS_DMA_TRACEO_PMS_R_REG (0x01CC)
```

| 31 | 0 |
|-----|---|
|     | Reset |
|     | 0xffffffff |

**PMS_DMA_TRACEO_R_PMS** Configures read permission for TRACEO to access 32 address ranges.

Bit 0 corresponds to region0, and so on.
- 0: Disable read permission.
- 1: Enable read permission.
(R/W)

Register 19.44. PMS_DMA_TRACEO_PMS_W_REG (0x01DO)
```

| 31 | 0 |
|-----|---|
|     | Reset |
|     | 0xffffffff |

**PMS_DMA_TRACEO_W_PMS** Configures write permission for TRACEO to access 32 address ranges.

Bit 0 corresponds to region0, and so on.
- 0: Disable write permission.
- 1: Enable write permission.
(R/W)
```