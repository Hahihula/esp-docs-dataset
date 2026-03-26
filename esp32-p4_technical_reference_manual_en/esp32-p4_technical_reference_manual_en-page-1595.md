

```markdown
| YUV422 | 2 x 1 | 1 x 1 | 1 x 1 |
|--------|-------|-------|-------|
| YUV420 | 2 x 2 | 1 x 1 | 1 x 1 |
| GRAY   | 1 x 1 | none  | none  |

¹ The MCU of each image format is represented by the number of data units in the horizontal direction x the number of data units in the vertical direction of each component.

At a time, the JPEG codec can only be configured as an encoder or a decoder, that is, it cannot work as an encoder and a decoder at the same time.

* When used as an encoder, it obtains the image to be compressed through 2D DMA and sends the encoded bitstream to the 2D DMA.
* When used as a decoder, it obtains the coded bitstream through 2D DMA and sends the decoded image to 2D DMA.

The workflow of JPEG codec is shown in Figure 35.2-1.

JPEG CODEC

Figure 35.2-1. JPEG codec system connection block diagram

The function clock of the JPEG codec is SYS_CLK.
```

### 35.3 Features

When used as an encoder, the JPEG codec has the following features:

* integrated discrete cosine transform algorithm
* integrated canonical Huffman coding
* RGB888, RGB565, YUV422 and GRAY as original input image formats
* conversion of RGB888 and RGB565 into YUV444, YUV422 or YUV420 (the only formats supported by impression) for image compression

Espressif Systems 1595 ESP32-P4 TRM PRELIMINARY Submit Documentation Feedback
```