

```markdown
| Bit | Name                                 | Description                                                                                                                                                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                                                                                                                                                             |
| 30  | DMA2D_IN_DONE_CHn_INT_ENA           | Write 1 to enable the DMA2D_IN_DONE_CHn_INT. (R/W)                                                                                                |
| 29  | DMA2D_IN_SUC_EOF_CHn_INT_ENA        | Write 1 to enable the DMA2D_IN_SUC_EOF_CHn_INT. (R/W)                                                                                               |
| 28  | DMA2D_IN_ERR_EOF_CHn_INT_ENA        | Write 1 to enable the DMA2D_IN_ERR_EOF_CHn_INT. (R/W)                                                                                              |
| 27  | DMA2D_IN_DSCR_ERR_CHn_INT_ENA       | Write 1 to enable the DMA2D_IN_DSCR_ERR_CHn_INT. (R/W)                                                                                            |
| 26  | DMA2D_INFIFO_OVF_L1_CHn_INT_ENA     | Write 1 to enable the DMA2D_INFIFO_OVF_L1_CHn_INT. (R/W)                                                                                           |
| 25  | DMA2D_INFIFO_UDF_L1_CHn_INT_ENA     | Write 1 to enable the DMA2D_INFIFO_UDF_L1_CHn_INT. (R/W)                                                                                           |
| 24  | DMA2D_INFIFO_OVF_L2_CHn_INT_ENA     | Write 1 to enable the DMA2D_INFIFO_OVF_L2_CHn_INT. (R/W)                                                                                           |
| 23  | DMA2D_INFIFO_UDF_L2_CHn_INT_ENA     | Write 1 to enable the DMA2D_INFIFO_UDF_L2_CHn_INT. (R/W)                                                                                           |
| 22  | DMA2D_INFIFO_OVF_L3_CHn_INT_ENA     | Write 1 to enable the DMA2D_INFIFO_OVF_L3_CHn_INT. (R/W)                                                                                           |
| 21  | DMA2D_INFIFO_UDF_L3_CHn_INT_ENA     | Write 1 to enable the DMA2D_INFIFO_UDF_L3_CHn_INT. (R/W)                                                                                           |
| 20  | DMA2D_IN_DSCR_EMPTY_CHn_INT_ENA      | Write 1 to enable the DMA2D_IN_DSCR_EMPTY_CHn_INT. (R/W)                                                                                            |
| 19  | DMA2D_INFIFO_RO_OVF_CHO_INT_ENA     | Write 1 to enable the DMA2D_INFIFO_RO_OVF_CHO_INT. (R/W)                                                                                           |
| 18  | DMA2D_INFIFO_RO_UDF_CHO_INT_ENA      | Write 1 to enable the DMA2D_INFIFO_RO_UDF_CHO_INT. (R/W)                                                                                            |
| 17  | DMA2D_IN_DSCR_TASK_OVF_CHn_INT_ENA | Write 1 to enable the DMA2D_IN_DSCR_TASK_OVF_CHn_INT. (R/W)                                                                                        |

Register 6.44. DMA2D_IN_INT_ENA_CHn_REG (n: 0-2) (0x0508+0x100*n)
```