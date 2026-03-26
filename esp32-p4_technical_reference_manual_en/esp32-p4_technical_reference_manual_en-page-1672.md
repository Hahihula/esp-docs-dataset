

```markdown
Register 36.3. ISP_CNTL_REG (0x0008)

Continued from the previous page...

ISP_CROP_EN Configures whether to enable the CROP module.
O: Disable
1: Enable
(R/W)

ISP_WBG_EN Configures whether to enable the WBG module.
O: Disable
1: Enable
(R/W)

ISP_BYTE_ENDIAN_ORDER Configures the byte order for MIPI Image Interface 32 input when ISP is disabled.
O: csi_data[31:0]
1: [7:0], [15:8], [23:16], [31:24]
(R/W)

ISP_DATA_TYPE Configures the input data type.
O: RAW8
1: RAW10
2: RAW12
3: invalid
(R/W)

ISP_IN_SRC Configures the input data source.
O: MIPI Image Interface 32 data from CSI HOST
1: Data from DVP
2: Data from VDMA
3: invalid
(R/W)

ISP_OUT_TYPE Configures the output data type.
O: RAW8
1: YUV422
2: RGB888
3: YUV420
4: RGB565
Others: Invalid
(R/W)
```