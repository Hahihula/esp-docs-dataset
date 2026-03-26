

```markdown
## Chapter 6 2D-DMA Controller (2D-DMA)

Figure 6.4-4. Macroblock Layout of JPEG Decoder Output Data

### 6.4.7 Color Space Conversion

On the transmit side, the 2D-DMA converts the color space after assembling the data read from memory into pixels. The 2D-DMA supports the following conversion except YUV420:

* RGB888 to RGB565
* RGB565 to RGB888
* RGB888 to YUV444
* RGB888 to YUV422 (the number of pixels per row in RGB format must be even)
* YUV444 to RGB888
* YUV422 to RGB888

On the receive side, only pixels received from JPEG requires color space conversion. The 2D-DMA supports the following conversion:

* YUV444 to RGB888/RGB565/YUV422/YUV420
* YUV422 to YUV444 to RGB888/RGB565/YUV420
* YUV420 to YUV444 to RGB888/RGB565

**Note:**
* For JPEG decoding, i.e., the receive side of 2D-DMA, the hardware will forcibly convert YUV422 and YUV420 to the YUV444 format. Software can optionally further convert the format to RGB888/RGB565 with the color space conversion feature.

Figure 6.4-5 shows the structure of the color space conversion module.
```