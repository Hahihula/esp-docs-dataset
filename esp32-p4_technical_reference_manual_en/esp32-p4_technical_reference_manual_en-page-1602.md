

```markdown
| JPEG_COMPONENT_NUM | JPEG_Cn_X/Y_FACTOR | Format of the Image to be Decoded |
|--------------------|---------------------|-----------------------------------|
| 0                  | -                   | invalid                           |
| 1                  | CO_X_FACTOR is 1    | GRAY                              |
|                    | CO_Y_FACTOR is 1    |                                   |
| 2                  | -                   | invalid                           |
|                    | CO_X_FACTOR is 1    |                                   |
|                    | CO_Y_FACTOR is 1    |                                   |
|                    | C1_X_FACTOR is 1    |                                   |
|                    | C1_Y_FACTOR is 1    | YUV444                            |
|                    | C2_X_FACTOR is 1    |                                   |
|                    | C2_Y_FACTOR is 1    |                                   |
| 3                  | CO_X_FACTOR is 2    |                                   |
|                    | CO_Y_FACTOR is 1    |                                   |
|                    | C1_X_FACTOR is 1    | YUV422                            |
|                    | C1_Y_FACTOR is 1    |                                   |
|                    | C2_X_FACTOR is 1    |                                   |
|                    | C2_Y_FACTOR is 1    |                                   |
|                    | CO_X_FACTOR is 2    |                                   |
|                    | CO_Y_FACTOR is 2    |                                   |
|                    | C1_X_FACTOR is 1    | YUV420                            |
|                    | C1_Y_FACTOR is 1    |                                   |
|                    | C2_X_FACTOR is 1    |                                   |
|                    | C2_Y_FACTOR is 1    |                                   |
```

Regardless of the format of the image to be decoded, the decoder only supports one scan, which contains all components. After decoding, the image will be sent to 2D DMA, so please refer to Chapter 6 2D-DMA Controller (2D-DMA) for the layout of the decoded image in each format.

### 35.5.2.2 Parsing RST Marker

The bitstream may have a restart (RST) marker in the scan segment. The RST marker code is `0xFFDx` (`x = 0, 1, ..., 7`).

JPEG decoder's hardware can parse RST markers and check whether the actual number of MCUs between two RST markers is the same as the restart interval defined in the DRI segment of the Tables/Miscellaneous segment.

Firstly, the software parses the DRI segment and pass the defined restart interval to register `JPEG_RESTART_INTERVAL`. Then, the hardware will check whether the subsequent bitstream has an RST marker every time `JPEG_RESTART_INTERVAL` MCUs are decoded.
```