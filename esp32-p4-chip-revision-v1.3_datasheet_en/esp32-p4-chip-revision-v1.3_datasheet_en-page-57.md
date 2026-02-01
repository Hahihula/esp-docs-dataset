**Title: Functional Description**

- **YUV422:** The horizontal resolution of the output decoded image is multiples of 16 and the vertical resolution is multiples of 8, i.e., 150 x 150 images with an output resolution of 160 x 152.
  
- **YUV420:** Both the horizontal and vertical resolutions of the output decoded image are multiples of 16, i.e., 150 x 150 images with an output resolution of 160 x 160.

**Performance:**
- Still image decoding: up to 4K resolution
- Dynamic image decoding: up to 1080P@40fps, 720P@70fps (excluding header parsing time)

**Pin Assignment**

The JPEG Codec does not interact directly with IOs, so it has no pins assigned.

**Subtitle: Image Signal Processor (ISP)**

ESP32-P4 includes an image signal processor (ISP), which is a pipeline composed of various image processing algorithms.

**Feature List**
- Maximum resolution: 1920 x 1080
- Three input channels: MIPI-CSI, DVP, and AXI-DMAC
- Input formats: RAW8, RAW10, and RAW12
- Output formats: RAW8, RGB888, RGB565, YUV422, and YUV420

**Pipeline features:**
  - Bayer filter (BF)
  - Demosaic
  - Color correction matrix (CCM)
  - Gamma correction
  - RGB2YUV
  - Sharpen
  - Contrast/hue/saturation/luminance adjustment (COLOR)
  - YUV_limit
  - YUV2RGB
  - Automatic exposure statistics (AE)
  - Automatic focus statistics (AF)
  - Automatic white balance statistics (AWB)
  - Histogram statistics (HIST)

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number and Document Version:** ESP32-P4 Series Datasheet v0.6, Page 57