

```markdown
- Automatic white balance statistics (AWB)
- Histogram statistics (HIST)

## 36.4 Architectural Overview

ISP architecture is shown in Figure 36.4-1, consisting of ISP_Header, ISP_Pipeline, ISP_Tail, and CSI_Bridge.

![Figure 36.4-1. ISP IP Architecture](image_path_if_available)

*   ISP_Header selects data from various input sources based on the configuration and buffers it. Then it transmits the buffered data to ISP_Pipeline in a standardized format.
*   ISP_Pipeline serves as the core module of the ISP, containing all the algorithms for image processing.
*   ISP_Tail has two input sources, MIPI-CSI and ISP_Pipeline. When ISP is disabled, Image Interface 32 data from MIPI-CSI is converted into Image Interface 64 format by ISP_Tail and transmitted to CSI_Bridge. When ISP is enabled, the output of ISP_Pipeline is cropped and converted into Image Interface 64 format by ISP_Tail, and then transmitted to CSI_Bridge.
*   As the output of the ISP, CSI_Bridge transmits the images from ISP to the system memory through VDMA.

## 36.5 Functional Description

### 36.5.1 ISP_Header

ISP_Header serves as the input of ISP. The main features are:

*   Select image data as input source based on the configuration of `ISP_IN_SRC`
*   Buffer image data, and convert images to the format required by ISP_Pipeline based on the configured type and size of image data
```