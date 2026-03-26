

```markdown
Register 40.26. CSI_HOST_INT_FORCE_SEQ_FRAME_FATAL_REG (0x0298)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             | Reset                                                                       |
| 30-0| reserved                                   |                                                                             |
| 15  | CSI_HOST_FORCE_ERR_F_SEQ_VC15              | Configures whether to force set CSI_HOST_ST_ERR_F_SEQ_VCn to 1.             |
| 14  | CSI_HOST_FORCE_ERR_F_SEQ_VC14              |                                                                             |
| 13  | CSI_HOST_FORCE_ERR_F_SEQ_VC13              |                                                                             |
| 12  | CSI_HOST_FORCE_ERR_F_SEQ_VC12              |                                                                             |
| 11  | CSI_HOST_FORCE_ERR_F_SEQ_VC11              |                                                                             |
| 10  | CSI_HOST_FORCE_ERR_F_SEQ_VC10              |                                                                             |
| 9   | CSI_HOST_FORCE_ERR_F_SEQ_VC9               |                                                                             |
| 8   | CSI_HOST_FORCE_ERR_F_SEQ_VC8               |                                                                             |
| 7   | CSI_HOST_FORCE_ERR_F_SEQ_VC7               |                                                                             |
| 6   | CSI_HOST_FORCE_ERR_F_SEQ_VC6               |                                                                             |
| 5   | CSI_HOST_FORCE_ERR_F_SEQ_VC5               |                                                                             |
| 4   | CSI_HOST_FORCE_ERR_F_SEQ_VC4               |                                                                             |
| 3   | CSI_HOST_FORCE_ERR_F_SEQ_VC3               |                                                                             |
| 2   | CSI_HOST_FORCE_ERR_F_SEQ_VC2               |                                                                             |
| 1   | CSI_HOST_FORCE_ERR_F_SEQ_VC1               |                                                                             |
| 0   | CSI_HOST_FORCE_ERR_F_SEQ_VC0               |                                                                             |

CSI_HOST_FORCE_ERR_F_SEQ_VCn (n: 0-15) Configures whether to force set CSI_HOST_ST_ERR_F_SEQ_VCn to 1.
0: Do not force set
1: Force set
(R/W)

Register 40.27. CSI_HOST_INT_ST_CRC_FRAME_FATAL_REG (0x02A0)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             | Reset                                                                       |
| 30-0| reserved                                   |                                                                             |
| 15  | CSI_HOST_ST_ERR_FRAME_DATA_VC15            | Represents whether the ERR_FRAME_DATA_VCn error occurs.                    |
| 14  | CSI_HOST_ST_ERR_FRAME_DATA_VC14            |                                                                             |
| 13  | CSI_HOST_ST_ERR_FRAME_DATA_VC13            |                                                                             |
| 12  | CSI_HOST_ST_ERR_FRAME_DATA_VC12            |                                                                             |
| 11  | CSI_HOST_ST_ERR_FRAME_DATA_VC11            |                                                                             |
| 10  | CSI_HOST_ST_ERR_FRAME_DATA_VC10            |                                                                             |
| 9   | CSI_HOST_ST_ERR_FRAME_DATA_VC9             |                                                                             |
| 8   | CSI_HOST_ST_ERR_FRAME_DATA_VC8             |                                                                             |
| 7   | CSI_HOST_ST_ERR_FRAME_DATA_VC7             |                                                                             |
| 6   | CSI_HOST_ST_ERR_FRAME_DATA_VC6             |                                                                             |
| 5   | CSI_HOST_ST_ERR_FRAME_DATA_VC5             |                                                                             |
| 4   | CSI_HOST_ST_ERR_FRAME_DATA_VC4             |                                                                             |
| 3   | CSI_HOST_ST_ERR_FRAME_DATA_VC3             |                                                                             |
| 2   | CSI_HOST_ST_ERR_FRAME_DATA_VC2             |                                                                             |
| 1   | CSI_HOST_ST_ERR_FRAME_DATA_VC1             |                                                                             |
| 0   | CSI_HOST_ST_ERR_FRAME_DATA_VC0             |                                                                             |

CSI_HOST_ST_ERR_FRAME_DATA_VCn (n: 0-15) Represents whether the ERR_FRAME_DATA_VCn error occurs.
0: Do not occur
1: Occur
(RC)
```