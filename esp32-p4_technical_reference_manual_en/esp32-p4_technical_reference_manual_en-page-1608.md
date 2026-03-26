

```markdown
- 0: disable
- 1: enable

* Select the image format to be compressed by configuring JPEG_SAMPLE_SEL:
    - 0: YUV444
    - 1: YUV422
    - 2: YUV420

Note that this register is valid only when the original image format is RGB, YUV444, or YUV422. See details in Table 35.5-1.

* Configure JPEG_HA as the original image width and JPEG_VA as the original image height.
* Configure the quantization coefficient table by following the instructions in Section 35.5.1.3.

3. Configure 2D DMA (For detailed instructions or introduction to related concepts, please refer to Chapter 6 2D-DMA Controller (2D-DMA).)

(a) Configure the linked list of 2D DMA TX channel.
    * Set 2DEN to 1 to enable 2D function.
    * Configure the Buffer address pointer as the starting address where the original image is stored.
    * Configure pbyte to select the number of bytes of one pixel of the original image.
    * Configure HA as the width of the original image and VA as the height of the original image.
    * Configure hb as the number of pixels in the horizontal direction of an image block and vb as the number of pixels in the vertical direction of an image block.
    * Configure mod as 1, which means continuous reading of image blocks of hb × vb size.
    * Configure (X, Y) as the coordinate of the first pixel in the starting image block. Among them, according to the original image format and the format of the image to be compressed, there are restrictions on hb and vb, as shown in the table 35.7-1:

Table 35.7-1. JPEG Encoder hb and vb Configuration

| Format of Original Image | Format of the Image to be Compressed | hb | vb |
|--------------------------|--------------------------------------|----|----|
| RGB/YUV444               | YUV444                               | Multiples of 8 | Multiples of 8 |
|                          | YUV422                               | Multiples of 16 | Multiples of 8 |
|                          | YUV420                               | Multiples of 16 | Multiples of 16 |
| YUV422                   | YUV422                               | Multiples of 16 | Multiples of 8 |
|                          | YUV420                               | Multiples of 16 | 16 |
| YUV420                   | YUV420                               | Multiples of 16 | 16 |
| GRAY                     | GRAY                                 | Multiples of 8 | Multiples of 8 |

(b) Configure the linked list of the 2D DMA RX channel:
    * Set 2DEN to 0 to enable 1D function.
```