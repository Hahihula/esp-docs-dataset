

# Chapter 36
## Image Signal Processor (ISP)

### 36.1 Introduction

ESP32-P4 includes an image signal processor (ISP), which is a pipeline composed of various image processing algorithms.

ISP reads image data from the DVP or MIPI-CSI camera interface, or from the system memory directly, and writes the processed image data to the system memory through VDMA.

The SoC architecture of ISP is shown in Figure 36.1-1. ISP must work with other modules to read and write data and can not work alone.

* When outputting images, ISP uses CSI_Bridge to convert data to AXI interface and stores the images to system memory through the VDMA controller. For more information about VDMA, see Chapter 5 VDMA Controller (VDMA)
* When the input image comes from the system memory, ISP must acquire the image data through VDMA
* When the input image comes from the MIPI-CSI camera interface,
    - ISP must acquire the image data through CSI HOST. For details, see Chapter 40 MIPI CSI
        - CSI_CM can preprocess it to perform 8-bit or 16-bit bit-swapping, color-channel reordering for RGB888, RGB565, or YUV422, downsample RGB888 to RGB565, or downsample YUV422 to YUV420
* When the input image comes from the DVP camera interface, ISP acquire the image data through the DVP IO. For details, see Chapter 9 GPIO Matrix and IO MUX

Figure 36.1-1. ESP32-P4 ISP SoC Architecture