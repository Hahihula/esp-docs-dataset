

```markdown
| Lane | Initial Seed Value |
|------|--------------------|
| 1    | 0x1008             |
| 2    | 0x1188             |

## 40.5.5 Error Management

The MIPI CSI-2 host analyzes received packets to identify protocol errors. Possible errors are listed in Table 40.5-6. These errors serve as interrupt sources and can generate the CSI_INTR signal. See Section 40.6 Interrupts for more details.

Table 40.5-6. Detectable Errors by MIPI CSI-2 Host

| Error/Interrupt Source                  | Description                                                                                      | Corresponding Register Field                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| PHY_ERRSOTSYNCHS_n (n: 0-1)              | Start-of-transmission error (no synchronization achieved) on data lane n                       | CSI_HOST_ST_PHY_ERRSOTSYNCHS_n (n: 0-1)                          |
| ERR_ECC_DOUBLE                           | Header ECC contains at least two errors (unrecoverable)                                         | CSI_HOST_ST_ERR_ECC_DOUBLE                                       |
| SHORTER_PAYLOAD                          | Reported word count exceeds received word count (unrecoverable)                                 | CSI_HOST_ST_SHORTER_PAYLOAD                                      |
| ERR_F_BNDRY_MATCH_VCn (n: 0-15)           | Error matching frame start with frame end for virtual channel n                                  | CSI_HOST_ST_ERR_F_BNDRY_MATCH_VCn (n: 0-15)                       |
| ERR_F_SEQ_VCn (n: 0-15)                   | Incorrect frame sequence detected on virtual channel n                                           | CSI_HOST_ST_ERR_F_SEQ_VCn (n: 0-15)                               |
| ERR_FRAME_DATA_VCn (n: 0-15)              | At least one CRC error in the last received frame on virtual channel n                           | CSI_HOST_ST_ERR_FRAME_DATA_VCn (n: 0-15)                         |
| ERR_CRC_VCn (n: 0-15)                    | Payload CRC error detected on virtual channel n                                                 | CSI_HOST_ST_ERR_CRC_VCn (n: 0-15)                                 |
| ERR_ID_VCn (n: 0-15)                     | Unrecognized or unimplemented data type detected on virtual channel n                           | CSI_HOST_ST_ERR_ID_VCn (n: 0-15)                                  |
```