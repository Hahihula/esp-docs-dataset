

```markdown
- 4 x configurable quantization coefficient tables with 8-bit or 16-bit precision
- performance:
    - still image compression: up to 4K resolution
    - dynamic image compression: up to 1080P@40fps,720P@70fps (excluding header encoding time)
- automatically added stuffed zero byte
- automatically added EOI marker

When used as a decoder, the JPEG codec has the following features:
- integrated inverse discrete cosine transform algorithm
- integrated Huffman decoding
- supported image formats for compressed bitstream decoding: YUV444, YUV422, YUV420, and GRAY.
- 4 x configurable quantization coefficient tables with 8-bit or 16-bit precision
- 2 x DC and 2 x AC Huffman tables
- supports image decoding of any resolution. However, the resolution of output decoded image differs from the format of the input image:
    - YUV444, GRAY: both the horizontal and vertical resolutions of the output decoded image are multiples of 8, i.e., 150 × 150 images with an output resolution of 152 × 152
    - YUV422: the horizontal resolution of the output decoded image is the multiples of 16 and the vertical resolution is multiples of 8, i.e., 150 × 150 images with an output resolution of 160 × 152
    - YUV420: both the horizontal and vertical resolutions of the output decoded image are multiples of 16, i.e., 150 × 150 images with an output resolution of 160 × 160
- performance:
    - still image decoding: up to 4K resolution
    - dynamic image decoding: up to 1080P@40fps,720P@70fps (excluding header parsing time)
```

## 35.4 Architectural Overview

When the JPEG codec is configured as an encoder, its architecture is shown in Figure 35.4-1.

![Figure 35.4-1. JPEG encoder architecture](image_path)  
*ENCODER DECODER common module*

**Figure 35.4-1. JPEG encoder architecture**
```