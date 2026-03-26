

```markdown
- Input formats: ARGB8888, RGB888, RGB565, YUV422, YUV420, GRAY
- Output formats: ARGB8888, RGB888, RGB565, YUV422, YUV420, GRAY
- Counterclockwise rotation angles: 0°, 90°, 180°, 270°
- Horizontal and vertical scaling with scaling factors of 8-bit integer part and 4-bit fractional part
- Horizontal and vertical mirroring

• Blending two layers of the same size and filling images with specific pixels by BLEND:
    - Foreground input formats: ARGB8888, RGB888, RGB565, L4, L8, A4, A8
    - Background input formats: ARGB8888, RGB888, RGB565, YUV422, YUV420, GRAY, L4, L8
    - Output formats: ARGB8888, RGB888, RGB565, YUV422, YUV420, GRAY
    - Layer blending based on the Alpha channel. If layers lack an Alpha channel, it can be provided through register configuration.
    - Special color filtering by setting color-key ranges of foreground and background layers

## 37.4 Architectural Overview

As shown in figure 37.4-1, there are two independent functional modules in PPA: SRM and BLEND.

![Figure 37.4-1. PPA Architecture](image_path_if_available)

For SRM, SRM Coordinate Calculation scans coordinates of the output pixel blocks and calculates coordinates of the corresponding input pixel blocks. Addr Gen calculates the address according to the input pixel block coordinates and sends them to 2D-DMA. After that, the PPA receives the pixel block data from 2D-DMA, converts it into ARGB8888 format according to the register configuration, and stores it into the RX FIFO (a ping-pong FIFO composed of two SRAMs, each of which can store the whole pixel block). When a complete
```