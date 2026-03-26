

```markdown
- HP L2MEM (0x4FF0_0000~0x4FFB_FFFF).
- external flash (0x4000_0000 ~ 0x43FF_FFFF).
- external RAM (0x4800_0000 ~ 0x4BFF_FFFF).

Additionally, VDMA Master 1 can also access:

- MIPI CSI internal memory (0x5010_4000 ~ 0x5010_4FFF).
- MIPI DSI internal memory (0x5010_5000 ~ 0x5010_5FFF).

Note:
When accessing a memory via DMA, a corresponding access permission is needed, otherwise this access may fail.
For more information about permission control, please refer to Chapter 19 Permission Control (PMS).
```

## 7.3.5 Modules/Peripherals Address Mapping

Table 7.3-2 lists all the modules/peripherals and their respective address ranges. Note that the address space of specific modules/peripherals is defined by “Boundary Address” (including both Low Address and High Address).

Table 7.3-2. Module/Peripheral Address Mapping

| Target | Boundary Address Low Address | High Address | Size (KB) |
|--------|------------------------------|--------------|-----------|
| HP CPU Peripherals (HP CPU PERI) |                              |              |           |
| Reserved | 0x3FF0_0000                 | 0x3FF0_3FFF |           |
| RISC-V Trace Encoder 0 | 0x3FF0_4000                 | 0x3FF0_4FFF | 4         |
| RISC-V Trace Encoder 1 | 0x3FF0_5000                 | 0x3FF0_5FFF | 4         |
| Bus Monitor | 0x3FF0_6000                 | 0x3FF0_6FFF | 4         |
| Reserved | 0x3FF0_7000                 | 0x3FF0_DFFF |           |
| L2MEM Monitor | 0x3FF0_E000                 | 0x3FF0_EFFF | 4         |
| SPM Monitor | 0x3FF0_F000                 | 0x3FF0_FFFF | 4         |
| HP Peripherals 0 (HP PERIO) |                              |              |           |
| USB 2.0 OTG High-Speed | 0x5000_0000                 | 0x5003_FFFF | 256       |
| USB 2.0 OTG Full-Speed | 0x5004_0000                 | 0x5007_FFFF | 256       |
| USB 2.0 OTG Full-Speed PHY | 0x5008_0000                 | 0x5008_0FFF | 4         |
| VDMA Controller | 0x5008_1000                 | 0x5008_1FFF | 4         |
| Reserved | 0x5008_2000                 | 0x5008_2FFF |           |
| SD/MMC Host Controller | 0x5008_3000                 | 0x5008_3FFF | 4         |
| H264 Encoder | 0x5008_4000                 | 0x5008_4FFF | 4         |
| GDMA-AHB | 0x5008_5000                 | 0x5008_5FFF | 4         |
| JPEG Codec | 0x5008_6000                 | 0x5008_6FFF | 4         |
| Pixel-Processing Accelerator (PPA) | 0x5008_7000                 | 0x5008_7FFF | 4         |
| 2D-DMA Controller | 0x5008_8000                 | 0x5008_8FFF | 4         |
| Key Manager | 0x5008_9000                 | 0x5008_9FFF | 4         |

Cont’d on next page
```