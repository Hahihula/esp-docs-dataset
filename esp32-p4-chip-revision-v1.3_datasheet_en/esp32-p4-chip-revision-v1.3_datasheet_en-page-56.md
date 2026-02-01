**Title: Functional Description**

---

### **4.2 Peripherals**

This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

#### 4.2.1 Image Processing

This subsection describes the peripherals for image and voice processing.

##### Subsection Title:
4.2.1.1 JPEG Codec

ESP32-P4’s JPEG codec is an image codec, which is based on the JPEG baseline standard, for compressing (encoding) and decompressing (decoding) images to reduce the bandwidth required to transmit images or the space required to store images, making it possible to process large-resolution images.

#### Feature List

When used as an encoder, the JPEG codec has the following features:

- Integrated discrete cosine transform algorithm
- Integrated canonical Huffman coding
- RGB888, RGB565, YUV422 and GRAY as original input image formats
- Conversion of RGB888 and RGB565 into YUV444, YUV422 or YUV420 (the only formats supported by impression) for image compression

Four configurable quantization coefficient tables with 8-bit or 16-bit precision.

#### Performance:

- Still image compression: up to 4K resolution
- Dynamic image compression: up to 1080P@40fps,720P@70fps (excluding header encoding time)
- Automatically added stuffed zero byte
- Automatically added EOI marker

When used as a decoder, the JPEG codec has the following features:

- Integrated inverse discrete cosine transform algorithm
- Integrated Huffman decoding
- Supported image formats for compressed bitstream decoding: YUV444, YUV422, YUV420, and GRAY.
- Four configurable quantization coefficient tables with 8-bit or 16-bit precision
- Two DC and two AC Huffman tables

Supports image decoding of any resolution. However, the resolution of the output decoded image differs from the format of the input image:

- YUV444, GRAY: both the horizontal and vertical resolutions of the output decoded image are multiples of 8, i.e., 150 × 150 images with an output resolution of 152 × 152

---

Espressif Systems  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6