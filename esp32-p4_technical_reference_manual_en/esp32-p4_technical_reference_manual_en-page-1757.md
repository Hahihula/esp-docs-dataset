

```markdown
- YUVlimit to RGB in BT709
    - R = (208/256)Ylimit + (459/256)Vlimit − 63367/256
    - G = (298/256)Ylimit − (55/256)Ulimit − (136/256)Vlimit + 19681/256
    - B = (298/256)Ylimit + (541/256)Ulimit − 73918/256

When the output format is YUV420, the output YUV data range needs to be configured as full-range or limit-range via the PPA_YUV_TX_RANGE field, and the protocol used for YUV to RGB conversion needs to be configured as BT601 or BT709 via the PPA_RGB2YUV_PROTOCOL field. The conversion formulas are as follows:

- YUVlimit to YUVfull
    - Yfull = (298/256)Ylimit + 4768/256
    - Ufull = (291/256)Ulimit + 4550/256
    - Vfull = (291/256)Vlimit + 4550/256

- RGB to YUVlimit in BT601
    - Ylimit = (4096/256) + (66/256)R + (129/256)G + (25/256)B
    - Ulimit = (32768/256 − 38/256)R − (74/256)G + (112/256)B
    - Vlimit = (32768/256 + 112/256)R − (94/256)G − (18/256)B

- RGB to YUVlimit in BT709
    - Ylimit = (4096/256 + 47/256)R + (157/256 + 16/256)G + (16/256)B
    - Ulimit = (32768/256 − 26/256)R − (86/256)G + (112/256)B
    - Vlimit = (32768/256 + 112/256)R − (102/256)G − (10/256)B

### 37.5.1.2 BLEND Color Space

BLEND supports ARGB8888, RGB8888, RGB565, L4, L8, A4, and A8 foreground input formats, and ARGB8888, RGB8888, RGB565, YUV422, YUV420, GRAY, L4, L8 background input formats. The input color format of the foreground and background layers can be configured respectively via the PPA_BLEND0/1_RX_CM field.

Among the above input formats, A4 and A8 only support the foreground layer, and when the input format is L4 or A4, the size of the image block, hb, and the offset in the image, x, must be an even number. For the output format, BLEND supports ARGB8888, RGB8888, and RGB565, which can be configured via the PPA_BLEND_TX_CM field.

BLEND’s RGB conversion, byte conversion, and alpha channel configuration are consistent with SRM input. Additionally, when the foreground layer data format is A4 or A8, the input data will be Alpha channel values. In this case, if PPA_BLEND_BYPASS is set as 1, the foreground layer’s input Alpha value replaces the background layer’s Alpha channel and output. If set as 0, it will be a normal BLEND operation, and the foreground layer’s RGB values will be specified by PPA_BLEND_RGB_REG.

When the input data format is L4 or L8, it requires to first initialize the CLUT for BLEND. BLEND has two CLUTs with a depth of 256 and a width of 32. There are two initialization modes: FIFO and MEM.

- Write 0 to PPA_APB_FIFO_MASK to enter the FIFO mode.
```