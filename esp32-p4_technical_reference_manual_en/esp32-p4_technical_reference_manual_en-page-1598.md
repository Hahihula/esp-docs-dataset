

```markdown
Chapter 35 JPEG Codec

GoBack

35.5.1 JPEG Encoder

35.5.1.1 Pause

The JPEG encoder can be paused during the operation for other higher priority tasks. This feature is controlled by register field JPEG_PAUSE_EN.

* Set JPEG_PAUSE_EN to 1, the JPEG encoder will no longer output the bitstream to the 2D DMA RX channel.
* Set JPEG_PAUSE_EN back to 0, the JPEG encoder will be resumed, and output the bitstream normally.

35.5.1.2 Color Space Conversion

According to the standard, the image formats supported by the JPEG encoder are YUV444, YUV422, YUV420, and GRAY. However, ESP32-P4's JPEG encoder has integrated a color space conversion function to convert RGB888 and RGB565 formats into the above-mentioned image formats supported by the encoder before encoding. In this way, the range of supported image formats is expanded.

The color space conversion formulas for converting RGB to YUV are:

Y = (0.299 * R) + (0.587 * G) + (0.114 * B)
U = (-0.1687 * R) + (-0.3313 * G) + (0.5 * B) + 128
V = (0.5 * R) + (-0.4187 * G) + (-0.0813 * B) + 128

YUV formats only support downsampling. For example, YUV444 can remain unchanged or be downsampled to YUV422 or YUV420, and YUV422 can remain unchanged or be downsampled to YUV420.

The image format before conversion is represented by its format as well as pixel order. Table 35.5-1 demonstrates the representations of the supported image formats for color space conversion:
```