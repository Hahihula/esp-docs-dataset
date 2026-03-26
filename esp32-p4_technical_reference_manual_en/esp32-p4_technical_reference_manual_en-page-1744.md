

```markdown
Chapter 36 Image Signal Processor (ISP)

Register 36.151. CSI_BRIG_FRAME_CFG_REG (0x0014)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | reserved                        |
| 26  | CSIBRIG_VADR_NUM                |
| 25  |                                 |
| 24  |                                 |
| 23  | CSI_BRIG_HADR_NUM_CHECK         |
| 22  | CSI_BRIG_HAS_HSYNC_E            |
| 12  |                                 |
| 11  |                                 |
| 0   | Reset                           |

CSI_BRIG_VADR_NUM Configures the height of an image frame. Measurement unit: line. (R/W)

CSI_BRIG_HADR_NUM Configures the amount of 64-bit data in the width of an image frame. (R/W)

CSI_BRIG_HAS_HSYNC_E Configures whether the Image Interface 64 input includes HSYNC_START and HSYNC_END packets.
0: Not included
1: Included
(R/W)

CSI_BRIG_VADR_NUM_CHECK Configures whether to enable line number checking.
0: Disable
1: Enable
(R/W)

Register 36.152. CSI_BRIG_ENDIAN_MODE_REG (0x0018)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | reserved                        |
| 0   | Reset                           |

CSI_BRIG_BYTE_ENDIAN_ORDER Configures the byte order of 64-bit data.
0: Byte order remains unchanged
1: Reverse the high and low bytes
(R/W)
```