

```markdown
Register 4.75. AXI_DMA_OUT_INT_ENA_CHn_REG (n: 0-2) (0x0140+0x68*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | AXI_DMA_OUT_LINK_SWITCH_CHn_INT_ENA        | Write 1 to enable AXI_DMA_OUT_LINK_SWITCH_CHn_INT. (RO)                     |
| 29  | AXI_DMA_OUTFIFO_L3_OVF_CHn_INT_ENA         | Write 1 to enable AXI_DMA_OUTFIFO_L3_OVF_CHn_INT. (R/W)                    |
| 28  | AXI_DMA_OUTFIFO_L3_UDF_CHn_INT_ENA         | Write 1 to enable AXI_DMA_OUTFIFO_L3_UDF_CHn_INT. (R/W)                    |
| 27  | AXI_DMA_OUTFIFO_L2_OVF_CHn_INT_ENA         | Write 1 to enable AXI_DMA_OUTFIFO_L2_OVF_CHn_INT. (R/W)                    |
| 26  | AXI_DMA_OUTFIFO_L2_UDF_CHn_INT_ENA         | Write 1 to enable AXI_DMA_OUTFIFO_L2_UDF_CHn_INT. (R/W)                    |
| 25  | AXI_DMA_OUTFIFO_L1_OVF_CHn_INT_ENA         | Write 1 to enable AXI_DMA_OUTFIFO_L1_OVF_CHn_INT. (R/W)                    |
| 24  | AXI_DMA_OUTFIFO_L1_UDF_CHn_INT_ENA         | Write 1 to enable AXI_DMA_OUTFIFO_L1_UDF_CHn_INT. (R/W)                    |
| 23  | AXI_DMA_OUT_TOTAL_EOF_CHn_INT_ENA          | Write 1 to enable AXI_DMA_OUT_TOTAL_EOF_CHn_INT. (R/W)                     |
| 22  | AXI_DMA_OUT_DSCR_ERR_CHn_INT_ENA           | Write 1 to enable AXI_DMA_OUT_DSCR_ERR_CHn_INT. (R/W)                      |
| 21  | AXI_DMA_OUT_EOF_CHn_INT_ENA                | Write 1 to enable AXI_DMA_OUT_EOF_CHn_INT. (R/W)                           |
| 20  | AXI_DMA_OUT_DONE_CHn_INT_ENA               | Write 1 to enable AXI_DMA_OUT_DONE_CHn_INT. (R/W)                          |

```