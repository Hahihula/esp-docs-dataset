

```markdown
Register 36.57. ISP_CAM_CONF_REG (0x0118)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    | ISP_CAM_DE_ONLY | ISP_CAM_VSYNC_FILTER_EN | ISP_CAM_VSYNC_INV | ISP_CAM_HSYNC_INV | ISP_CAM_DATA_TYPE | ISP_CAM_2BYTE_MODE | Reset |
| Value | 0x2a | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |    |

ISP_CAM_DATA_ORDER Configures the order of DVP input data.
0: cam_data_in
1: cam_data_in[7:0], cam_data_in[15:8]
(R/W)

ISP_CAM_2BYTE_MODE Configures whether to enable the 2-byte mode.
0: Disable
1: Enable
(R/W)

ISP_CAM_DATA_TYPE Configures the format of DVP input data.
0x2a: RAW8
0x2b: RAW10
0x2c: RAW12
(R/W)

ISP_CAM_DE_INV Configures whether to invert the DVP de signal.
0: Not invert
1: Invert
(R/W)

ISP_CAM_HSYNC_INV Configures whether to invert the DVP hsync signal.
0: Not invert
1: Invert
(R/W)

ISP_CAM_VSYNC_INV Configures whether to invert the DVP vsync signal.
0: Not invert
1: Invert
(R/W)

ISP_CAM_VSYNC_FILTER_THRES Configures vsync filtering. Vsyncs shorter than this length will be filtered out. (R/W)
```