

```markdown
Among them, I_score_mb_cmp is the score of the luma component of the current MB calculated by ENC_CORE. H264_x_I16x16_DECSCORE_OFFSET is the configurable offset register.
H264_x_L_DECSCORE is the configurable threshold register. x can be A or B, indicating the register corresponding to video sequence A or B. When the above requirement is met, the quantization result of the current luma component MB will be decimated to 0.

- luma component I MB with 4 x 4 partition: Current luma component MB quantization result will not be decimated to 0.
- chroma component I MB:

    c_score_mb_cmp + H264_x_I_chroma_DECSCORE_OFFSET < H264_x_C_DECSCORE

Among them, c_score_mb_cmp is the score of current chroma component MB calculated by ENC_CORE. H264_x_I_chroma_DECSCORE_OFFSET is the configurable offset register.
H264_x_C_DECSCORE is the configurable threshold register. x can be A or B, indicating the register corresponding to video sequence A or B. When the above requirement is met, the quantization result of the current chroma component MB will be decimated to 0.

- luma component P MB:

    I_score_mb_cmp + H264_x_P16x16_DECSCORE_OFFSET < H264_x_L_DECSCORE

Among them, I_score_mb_cmp is the score of current luma component MB calculated by ENC_CORE.
H264_x_P16x16_DECSCORE_OFFSET is the configurable offset register. H264_x_L_DECSCORE is the configurable threshold register. x can be A or B, indicating the register corresponding to video sequence A or B. When the above requirement is met, the quantization result of the current luma component MB will be decimated to 0.

- chroma component P MB:

    c_score_mb_cmp + H264_x_P_chroma_DECSCORE_OFFSET < H264_x_C_DECSCORE

Among them, c_score_mb_cmp is the score of current chroma component MB calculated by ENC_CORE. H264_x_P_chroma_DECSCORE_OFFSET is the configurable offset register.
H264_x_C_DECSCORE is the configurable threshold register. x can be A or B, indicating the register corresponding to video sequence A or B. When the above requirement is met, the quantization result of the current chroma component MB will be decimated to 0.

## 39.5.1.3 Motion Vector (MV) Merging

The ENC_CORE merges the MVs of the luma MB according to the configuration of the registers related to MV merging, and writes it out to the RX channel 3 channel (rx_push_mv_merge) of H264_DMA, and finally stores it in the internal memory for the upper layer application use, such as motion detection.

The registers related to MV merging are as follows:

- **H264_x_MV_MERGE_EN**: This register controls the enablement of MV merging. Setting this register to 1 means enabling the MV merging function of the corresponding video sequence. Setting this register to 0 means turning off the MV merging function of the corresponding video sequence. x can be A or B, indicating the register corresponding to video sequence A or B. Even if the MV merging function is enabled, the I MB will not output any data to the memory because the I MB has no MV.
```