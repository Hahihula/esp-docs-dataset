

```markdown
| Field          | Configuration                                                                 |
|----------------|-------------------------------------------------------------------------------|
| owner          | 1                                                                             |
| eof            | 1                                                                             |
| 2DEN           | 1                                                                             |
| err_eof        | 0                                                                             |
| hb             | Horizontal size of the image block.<br>Must be even if the input or output data format is YUV420 |
| vb             | Vertical size of the image block.<br>Must be even if the input or output data format is YUV420 |
| pbyte          | ARGB8888: 5 (4 byte/pixel)<br>RGB888: 4 (3 byte/pixel)<br>RGB565: 3 (2 byte/pixel)<br>YUV420: 2 (1.5 byte/pixel)<br>A8/L8: 1 (1 byte/pixel)<br>A4/L4: 0 (0.5 byte/pixel) |
| HA             | Horizontal size of the entire image.<br>Must be even if the input or output data format is YUV420 |
| VA             | Vertical size of the entire image.<br>Must be even if the input or output data format is YUV420 |
| mod            | 0                                                                             |
| X              | Horizontal offset of the image block within the image (offset starts from 0).<br>Must be even if the input or output data is YUV420 |
| Y              | Vertical offset of the image block within the image (offset starts from 0).<br>Must be even if the input or output data is YUV420 |
| Buffer address pointer | Starting address of the image |
| Next descriptor address | N/A                                                                             |
```

### 37.5.2.1 SRM Special Configuration

Once the 2D-DMA linked lists for input and output image blocks are configured, SRM needs to select the required pixel blocks from the input image block memory space and process them in units of pixel blocks. The processed pixel blocks are then stored in the corresponding memory space of the output image block.

Throughout this process, the starting address of each pixel block needs to be controlled by SRM. To realize this functionality, write 1 to the `DMA2D_IN/OUT_DSCR_PORT_EN_CHx` field of the corresponding channel of the 2D-DMA to enable the descriptor interface (also called DSCR-PORT in 2D-DMA), allowing PPA to control
```