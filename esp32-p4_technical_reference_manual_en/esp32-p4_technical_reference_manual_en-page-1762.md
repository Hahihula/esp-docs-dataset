

```markdown
| Horizontal Size | Rearrangement Number | Horizontal Size | Rearrangement Number | Horizontal Size (Even) | Rearrangement Number |
|-----------------|----------------------|------------------|----------------------|------------------------|----------------------|
| 8               | 4                    | 8                | 8                    | 16                     | 4                    |
| 9               | 3                    | 9                | 7                    | 18                     | 3                    |
| 10              | 3                    | 10               | 6                    | 20-32                  | 2                    |
| 11              | 2                    | 11               | 5                    |                        |                      |
| 12              | 2                    | 12               | 5                    |                        |                      |
| 13              | 2                    | 13               | 4                    |                        |                      |
| 14              | 2                    | 14               | 4                    |                        |                      |
| 15              | 2                    | 15               | 4                    |                        |                      |
| 16              | 2                    | 16               | 4                    |                        |                      |
|                 |                      | 17               | 3                    |                        |                      |
|                 |                      | 18               | 3                    |                        |                      |
|                 |                      | 19-32            | 2                    |                        |                      |

## 37.5.4 Layer Blending (BLEND)

### 37.5.4.1 Basic Functionality

BLEND combines two image blocks of the same size using the Alpha channel and then outputs the result. The blending formula is as follows, where Ab is the Alpha channel of the background layer, Af is the Alpha channel of the foreground layer, Cb corresponds to the R, G, and B components of the background layer, and Cf corresponds to the R, G, B components of the foreground layer:

*   `Aout = Ab + Af - Ab * Af`
*   `Cout = (Cb * Ab * (1 - Af) + Cf * Af) / (Ab + Af - Ab * Af)`

Additionally, BLEND supports color-keying based on pixel color. By configuring color ranges via PPA_CK_FG/BG_HIGH/LOW_REG, BLEND allows for image segmentation into four distinct regions, each subjected to different operations:

*   When the foreground pixel falls within the color-key range and the background pixel falls outside the color-key range, output the background pixel.
*   When the background pixel falls within the color-key range and the foreground pixel falls outside the color-key range, the output depends on the value of PPA_COLORKEY_FG_BG_REVERSE. If 0, output the background pixel; if 1, output the foreground pixel.
*   When both the background and foreground pixels fall within the color-key range, the output is set to the color defined by PPA_COLORKEY_DEFAULT_R/G/B.
*   When neither the background nor foreground pixels fall within the color-key range, output follows the normal Alpha Blending process.

When PPA_BLEND_BYPASS is set to 1, BLEND directly outputs the background layer data. If the foreground input data type is A4/A8 at this time, the foreground input data will replace the background input data's Alpha channel and then be output.
```