

```markdown
sequence A or B. The calculation method of the configuration value of this register belongs to the category of the frame-level rate control algorithm in the software, which is beyond the scope of this chapter and will not be described.

*   H264_x_QP_MAX: This register is used to limit the maximum value of the QP finally calculated by the MB level rate control, and the value range is from 10 to 51. If the QP value finally calculated by the MB level rate control is greater than the configuration value of this register, it will be limited to the configured value of this register, otherwise the original value is retained. x can be A or B, indicating the register corresponding to video sequence A or B.
*   H264_x_QP_MIN: This register is used to limit the minimum value of the QP finally calculated by the MB level rate control, and the value range is from 10 to 51. If the QP value finally calculated by the MB level rate control is smaller than the configuration value of this register, it will be limited to the configured value of this register, otherwise it remains the original value, x can be A or B, indicating the register corresponding to video sequence A or B.
*   H264_FRAME_MAD_SUM: This register represents the cumulative sum of the MADs of all MBs in the current frame. The software needs to read the value of this register after the encoding of a frame of video is completed for calculation of frame-level rate control. The frame-level rate control algorithm in the software is beyond the scope of this chapter and will not be described.
*   H264_FRAME_ENC_BITS: This register represents the sum of the number of encoding bits of all MBs in the current frame. The software needs to read the value of this register after completely encoding a frame of video to perform frame-level rate control. The frame-level rate control algorithm in the software is beyond the scope of this chapter and will not be described.
*   H264_FRAME_QP_SUM: This register represents the sum of QP of all MBs in the current frame. The software needs to read the value of this register after completely encoding a frame of video to perform frame-level rate control. The frame-level rate control algorithm in the software is beyond the scope of this chapter and will not be described.

### 39.5.1.5 Region of Interest (ROI)

ENC_CORE can have up to 8 overlapping fixed-priority rectangular ROI in a frame of video according to the configuration of the relevant registers. The QP (calculated by MB level rate control) is adjusted, so that each ROI has different encoded picture quality.

The registers related to the ROI are as follows:

*   H264_x_ROI_EN: This register is used to control the switch of the ROI function. Set it to 1 to enable the ROI function, and set it to 0 to disable the ROI function. x can be A or B, indicating the register corresponding to video sequence A or B.
*   H264_x_ROI_MODE: This register is used to specify the working mode of ROI. If it is configured as 0, ROI will work in fixed QP mode. If it is configured as 1, ROI will work in QP offset mode. x can be A or B, indicating the register corresponding to video sequence A or B.
*   H264_x_ROI_REGIONn_REG: This register is used to configure the enable and position information of each rectangular ROI. x can be A or B, indicating the register corresponding to video sequence A or B. n can be 0 to 7, indicating 8 ROI. From ROI 0 to ROI 7, the priority decreases in order. When there are overlapping areas, the configuration of the ROI with the highest priority takes effect. This register contains the following fields:
```