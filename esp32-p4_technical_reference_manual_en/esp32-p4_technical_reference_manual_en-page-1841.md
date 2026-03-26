

```markdown
- H264_x_ROI_REGIONn_EN: Set to 1 to enable ROI n, set it to 0 to close the ROI n. When the register H264_x_ROI_LEN set to 1, this register can control the ROI n switch, otherwise, this register has no effect.
- H264_x_ROI_REGIONn_X: Configure the horizontal starting MB coordinates of the ROI n in a frame of video.
- H264_x_ROI_REGIONn_Y: Configure the vertical starting MB coordinates of the ROI n in a frame of video.
- H264_x_ROI_REGIONn_X_LEN: Configure the number of horizontal MBs in the ROI n in a frame of video.
- H264_x_ROI_REGIONn_Y_LEN: Configure the number of vertical MBs in the ROI n in a frame of video.

• H264_x_ROI_REGIONn_QP: This register is used to configure the QP adjustment amount of the MBs in each rectangular ROI. x can be A or B, indicating the register corresponding to video sequence A or B. n can be 0 to 7, representing 8 ROI. The configuration method of this register is related to the configuration value of the H264_x_ROI_MODE register:

    - When H264_x_ROI_MODE is set to 0: It means that the ROI mode is fixed QP mode. At this time, the value of H264_x_ROI_REGIONn_QP register is directly As the QP value of the MB in the corresponding ROI, the value range is 10 to 51.
    - When H264_x_ROI_MODE is set to 1: It indicates that the ROI mode is QP offset mode. At this time, bit 0 to bit 5 of the H264_x_ROI_REGIONn_QP register indicates the QP offset, and the value range is 0 to 51. Bit 6 indicates the sign of the offset, where 0 indicates a positive offset, and 1 indicates a negative offset.

• H264_x_NO_ROI_REGION_QP: This register is used to configure the QP offset of the MB in the non-ROI. Bit 0 to bit 5 represent the QP offset, and the value range is 0 to 51. Bit 6 represents the sign of the offset, where 0 represents a positive offset, and 1 indicates a negative offset. x can be A or B, indicating the register corresponding to video sequence A or B. When the ROI function is disabled, that is, when the H264_x_ROI_EN register is set to 0, this register will not take effect, and the QP of the MB in the non-ROI will not be changed.

Please note that the adjusted QP value of any ROI should not be less than 10.

Regardless of whether the MB is in the ROI or non-ROI, its final adjusted QP value will be limited to 0 to 51 to ensure that it does not exceed the value range in the H264 standard.
```

### 39.5.2 H264 Dedicated DMA

The H264 dedicated DMA controls the data transfers between encoder algorithm core and memory based on the software configuration.

#### 39.5.2.1 Architecture

H264_DMA architecture is shown in the figure 39.5-2:
```markdown
Espressif Systems                         1841                        ESP32-P4 TRM
Submit Documentation Feedback            PRELIMINARY
```