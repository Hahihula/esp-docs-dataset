

```markdown
GRAY | Multiples of 8 | 8 |
|---|---|---|

3. Configure 2D DMA (For detailed instructions or introduction to related concepts, please refer to Chapter 6 2D-DMA Controller (2D-DMA).)

(a) Configure the linked list of the 2D DMA TX channel.
* Set 2DEN to 0 to enable the 1D function.
* Configure the Buffer address pointer as the starting address where the bitstream to be decoded is stored.
* Configure the length and size as the number of bytes in the space to store the bitstream to be decoded.
* configure mod as 0, which means one-time reading of image blocks of hb x vb size.

(b) Configure the linked list of 2D DMA RX channel.
* Set 2DEN to 1 to enable 2D function.
* Configure the Buffer address pointer as the starting address where the decoded image will be stored.
* Configure pbyte to select the number of bytes of one pixel of the image which is decoded and has undergone 2D DMA color space conversion.
* Configure HA as the width of the output decoded image, configure VA as the height of the output decoded image, configure hb as the number of pixels in the horizontal direction of an image block, configure vb as the number of pixels in the vertical direction of an image block.
* Configure mod as 1, which means continuous reading of image blocks of hb x vb size.
* Configure (X, Y) as the coordinates of the first pixel in the starting image block. Among them, according to the decoded image format, there are restrictions on hb and vb, as shown in the table 35.7-4:

Table 35.7-4. JPEG Decoder hb and vb Configuration

<table><thead><tr><td>Decoded image format</td><td>hb</td><td>vb</td></tr></thead><tbody><tr><td>YUV444</td><td>Multiples of 8</td><td>Multiples of 8</td></tr><tr><td>YUV422</td><td>Multiples of 16</td><td>Multiples of 8</td></tr><tr><td>YUV420</td><td>Multiples of 16</td><td>Multiples of 16</td></tr><tr><td>GRAY</td><td>Multiples of 8</td><td>Multiples of 8</td></tr></tbody></table>

(c) Connect 2D DMA channels to JPEG codec:
* Connect the TX channeln to the JPEG codec by configuring DMA2D_OUT_PERI_SEL_CHn to 0;
* Connect the RX channeln to the JPEG codec by configuring DMA2D_IN_PERI_SEL_CHn to 0.

(d) Reset 2D DMA channels:
* 2D DMA TX channeln: set DMA2D_OUT_RST_CHn to 1 to reset 2D DMA TX channeln, then set DMA2D_OUT_RST_CHn to 0 to release the reset of 2D DMA TX channeln.
```