

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| Configuration Registers                    |                                                                                                  |           |        |
| H264_SYS_CTRL_REG                         | H264 system level control register                                                              | 0x0000    | varies |
| H264_GOP_CONF_REG                          | GOP related configuration register                                                             | 0x0004    | R/W    |
| H264_SLICE_HEADER_REMAIN_REG               | Frame slice header remain bit register                                                         | 0x00AC    | R/W    |
| H264_SLICE_HEADER_BYTE_LENGTH_REG          | Frame slice header byte length register                                                       | 0x00B0    | R/W    |
| H264_BS_THRESHOLD_REG                      | Bitstream buffer overflow threshold register                                                  | 0x00B4    | R/W    |
| H264_SLICE_HEADER_BYTE0_REG                | Frame slice header byte low 32 bit register                                                   | 0x00B8    | R/W    |
| H264_SLICE_HEADER_BYTE1_REG                | Frame slice header byte high 32 bit register                                                 | 0x00BC    | R/W    |
| H264_CONF_REG                              | General configuration register                                                                 | 0x00D0    | R/W    |
| H264_MV_MERGE_CONFIG_REG                   | MV merge configuration register                                                                | 0x00D4    | varies |
| Video Sequence A Configuration Registers   |                                                                                                  |           |        |
| H264_A_SYS_MB_RES_REG                      | Video sequence A horizontal and vertical MB resolution register                                | 0x0008    | R/W    |
| H264_A_SYS_CONF_REG                        | Video sequence A system level configuration register                                          | 0x000C    | R/W    |
| H264_A_DECSCORE_REG                        | Video sequence A luma and chroma MB decimate score register                                   | 0x0010    | R/W    |
| H264_A_DECSCORE_OFFSET_REG                 | Video sequence A luma and chroma MB decimate score offset register                            | 0x0014    | R/W    |
| H264_A_RC_CONF0_REG                        | Video sequence A rate control configuration register0                                        | 0x0018    | R/W    |
| H264_A_RC_CONF1_REG                        | Video sequence A rate control configuration register1                                        | 0x001C    | R/W    |
| H264_A_DB_BYPASS_REG                       | Video sequence A Deblocking bypass register                                                   | 0x0020    | R/W    |
| H264_A_ROI_REGIONO_REG                     | Video sequence A H264 ROI0 range configure register                                          | 0x0024    | R/W    |
| H264_A_ROI_REGION1_REG                     | Video sequence A H264 ROI1 range configure register                                          | 0x0028    | R/W    |
| H264_A_ROI_REGION2_REG                     | Video sequence A H264 ROI2 range configure register                                          | 0x002C    | R/W    |
```