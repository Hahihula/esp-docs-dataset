

```markdown
## Register 40.32. CSI_HOST_INT_FORCE_PLD_CRC_FATAL_REG (0x02B8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset | (reserved) |
| Name | CSI_HOST_FORCE_ERR_CRC_VC15 | CSI_HOST_FORCE_ERR_CRC_VC14 | CSI_HOST_FORCE_ERR_CRC_VC13 | CSI_HOST_FORCE_ERR_CRC_VC12 | CSI_HOST_FORCE_ERR_CRC_VC11 | CSI_HOST_FORCE_ERR_CRC_VC10 | CSI_HOST_FORCE_ERR_CRC_VC9 | CSI_HOST_FORCE_ERR_CRC_VC8 | CSI_HOST_FORCE_ERR_CRC_VC7 | CSI_HOST_FORCE_ERR_CRC_VC6 | CSI_HOST_FORCE_ERR_CRC_VC5 | CSI_HOST_FORCE_ERR_CRC_VC4 | CSI_HOST_FORCE_ERR_CRC_VC3 | CSI_HOST_FORCE_ERR_CRC_VC2 | CSI_HOST_FORCE_ERR_CRC_VC1 | 0 |

**Description:**  
`CSI_HOST_FORCE_ERR_CRC_VCn (n: 0-15)` Configures whether to force set `CSI_HOST_ST_ERR_CRC_VCn` to 1.  
- 0: Do not force set  
- 1: Force set  
(R/W)

## Register 40.33. CSI_HOST_INT_ST_DATA_ID_REG (0x02C0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset | (reserved) |
| Name | CSI_HOST_ST_ERR_ID_VC15 | CSI_HOST_ST_ERR_ID_VC14 | CSI_HOST_ST_ERR_ID_VC13 | CSI_HOST_ST_ERR_ID_VC12 | CSI_HOST_ST_ERR_ID_VC11 | CSI_HOST_ST_ERR_ID_VC10 | CSI_HOST_ST_ERR_ID_VC9 | CSI_HOST_ST_ERR_ID_VC8 | CSI_HOST_ST_ERR_ID_VC7 | CSI_HOST_ST_ERR_ID_VC6 | CSI_HOST_ST_ERR_ID_VC5 | CSI_HOST_ST_ERR_ID_VC4 | CSI_HOST_ST_ERR_ID_VC3 | CSI_HOST_ST_ERR_ID_VC2 | CSI_HOST_ST_ERR_ID_VC1 | 0 |

**Description:**  
`CSI_HOST_ST_ERR_ID_VCn (n: 0-15)` Represents whether the `ERR_ID_VCn` error occurs.  
- 0: Do not occur  
- 1: Occur  
(RC)
```