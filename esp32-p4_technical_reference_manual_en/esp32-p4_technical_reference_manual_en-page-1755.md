

```markdown
| Color Format          | Start Addr + 3       | Start Addr + 2 | Start Addr + 1 | Start Addr + 0 |
|-----------------------|----------------------|----------------|----------------|----------------|
| YUV422                |                      |                |                |                |
| YUV422_BYTE           |                      |                |                |                |
| _ORDER=1              |                      |                |                |                |
|                       |                      |                |                |                |
| YUV422                |                      |                |                |                |
| YUV422_BYTE           |                      |                |                |                |
| _ORDER=2              |                      |                |                |                |
|                       |                      |                |                |                |
| YUV422                |                      |                |                |                |
| YUV422_BYTE           |                      |                |                |                |
| _ORDER=3              |                      |                |                |                |
|                       |                      |                |                |                |
| YUV420                |                      |                |                |                |
| Odd rows              |                      |                |                |                |
| such as 1, 3, 5...    |                      |                |                |                |
| YUV420                |                      |                |                |                |
| Even rows             |                      |                |                |                |
| such as 2, 4, 6...    |                      |                |                |                |
| GRAY                  |                      |                |                |                |

### 37.5.1.1 SRM Color Space

SRM supports ARGB8888, RGB888, RGB565, and YUV422, YUV420, and GRAY formats for both input and output. The input format is configured by `PPA_SRM_RX_CM`, while the output format is configured by `PPA_SRM_TX_CM`. The SRM input pixel processing steps are shown in Figure 37.5-1.

![Figure 37.5-1. PPA SRM Input Pixel Processing](image_path_if_available)

SRM supports RGB and byte swapping for ARGB8888, RGB888, and RGB565 input formats. The specific configurations are as follows:

*   Set `PPA_SRM_RX_RGB_SWAP_EN` to 1 to reverse RGB to BGR and ARGB to BGRA.
*   Set `PPA_SRM_RX_BYTE_SWAP_EN` to 1 to reverse bytes 0, 1 and 2, 3 respectively, i.e., {0, 1, 2, 3} will be reverted to {1, 0, 3, 2}. RGB888 would not be affected by this configuration as it only has three bytes per pixel.

SRM uses ARGB8888 when processing images internally. When the input lacks an Alpha channel, the default Alpha channel value for the image is set to 255. The Alpha channel can be further configured using the `PPA_SRM_FIX_ALPHA_REG` register, as shown in Figure 37.5-2. For specific configuration effects, please refer to Table 37.5-2.
```