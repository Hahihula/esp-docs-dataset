

```markdown
| LUT sel | bit [19:10] | bit [9:0] |
|---------|-------------|-----------|
| LUT_Gb_B | Gb          | B         |
| LUT_R_Gr | R           | Gr        |

### 36.5.2.5 Demosaic

The demosaicing process converts Bayer images to RGB888 images. The conversion effect can be fine-tuned using `ISP_DEMOSAIC_GRAD_RATIO`. This register field comprises 2 integer bits and 4 fractional bits, with a default value of 1.0.

### 36.5.2.6 White Balance Gain (WBG)

This module performs white balance adjustment on the input image. The adjustment is achieved by multiplying the pixel value of each color channel by its corresponding `ISP_WBG_R/B/G` gain coefficient. Each
```