

```markdown
Chapter 19 Permission Control (PMS)

Register 19.35. PMS_DMA_USB_PMS_R_REG (0x01AC)
```

| 31 | PMS_DMA_USB_R_PMS | 0 |
|-----|-------------------|----|
|     |                   |    |
|     |                   | Reset |
|     |                   | 0xFFFFFF |

PMS_DMA_USB_R_PMS Configures read permission for high-speed USB 2.0 OTG to access 32 address ranges. Bit 0 corresponds to region0, and so on.
- O: Disable read permission.
- 1: Enable read permission.
(R/W)

Register 19.36. PMS_DMA_USB_PMS_W_REG (0x01B0)
```

| 31 | PMS_DMA_USB_W_PMS | 0 |
|-----|-------------------|----|
|     |                   |    |
|     |                   | Reset |
|     |                   | 0xFFFFFF |

PMS_DMA_USB_W_PMS Configures write permission for high-speed USB 2.0 OTG to access 32 address ranges. Bit 0 corresponds to region0, and so on.
- O: Disable write permission.
- 1: Enable write permission.
(R/W)
```