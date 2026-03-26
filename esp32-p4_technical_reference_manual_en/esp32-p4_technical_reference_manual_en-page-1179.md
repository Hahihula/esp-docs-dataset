

```markdown
Chapter 19 Permission Control (PMS)

Register 19.49. PMS_DMA_H264_PMS_R_REG (0x01FC)
```

| 31 | 0 |
|----|---|
| oxffffffff | Reset |

**PMS_DMA_H264_R_PMS**

Configures read permission for H264 DMA to access 32 address ranges.

Bit 0 corresponds to region0, and so on.

- 0: Disable read permission.
- 1: Enable read permission.

(R/W)

Register 19.50. PMS_DMA_H264_PMS_W_REG (0x0200)
```

| 31 | 0 |
|----|---|
| oxffffffff | Reset |

**PMS_DMA_H264_W_PMS**

Configures write permission for H264 DMA to access 32 address ranges.

Bit 0 corresponds to region0, and so on.

- 0: Disable write permission.
- 1: Enable write permission.

(R/W)
```