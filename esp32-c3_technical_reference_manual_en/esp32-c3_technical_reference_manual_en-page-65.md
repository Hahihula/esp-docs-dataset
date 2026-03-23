

```markdown
If the owner bit is O, the buffer is accessed by the CPU. In this case, the owner bit fails the check. The owner bit will not be checked if GDMA_IN_CHECK_OWNER_CHn or GDMA_OUT_CHECK_OWNER_CHn is 0;

* Buffer address pointer (DW1) check. If the buffer address pointer points to 0x3FC80000 ~ 0x3FCFFFFFF (please refer to Section 2.4.7), it passes the check.

After software detects a descriptor error interrupt, it must reset the corresponding channel, and enable GDMA by setting GDMA_OUTLINK_START_CHn or GDMA_INLINK_START_CHn bit.

Note: The third word (DW2) in a descriptor can only point to a location in internal RAM, given that the third word points to the next descriptor to use and that all descriptors must be in internal memory.
```

## 2.4.6 EOF

The GDMA controller uses EOF (end of frame) flags to indicate the end of data segment transfer corresponding to a specific descriptor.

Before the GDMA controller transmits data, GDMA_OUT_TOTAL_EOF_CHn_INT_ENA bit should be set to enable GDMA_OUT_TOTAL_EOF_CHn_INT interrupt. If data in the buffer pointed by the last descriptor (with EOF) has been transmitted, a GDMA_OUT_TOTAL_EOF_CHn_INT interrupt is generated.

Before the GDMA controller receives data, GDMA_IN_SUC_EOF_CHn_INT_ENA bit should be set to enable GDMA_IN_SUC_EOF_CHn_INT interrupt. If a data segment with an EOF flag has been received successfully, a GDMA_IN_SUC_EOF_CHn_INT interrupt is generated. In addition, when GDMA channel is connected to UHClO, the GDMA controller also supports GDMA_IN_ERR_CHn_EOF_INT interrupt. This interrupt is enabled by setting GDMA_IN_ERR_EOF_CHn_INT_ENA bit, and it indicates that a data segment corresponding to a descriptor has been received with errors.

When detecting a GDMA_OUT_TOTAL_EOF_CHn_INT or a GDMA_IN_SUC_EOF_CHn_INT interrupt, software can record the value of GDMA_OUT_EOF_DES_ADDR_CHn or GDMA_IN_SUC_EOF_DES_ADDR_CHn field, i.e. address of the last descriptor. Therefore, software can tell which descriptors have been used and reclaim them.

Note: In this chapter, EOF of transmit descriptors refers to suc_eof, while EOF of receive descriptors refers to both suc_eof and err_eof.

## 2.4.7 Accessing Internal RAM

Any transmit and receive channels of GDMA can access 0x3FC80000 ~ 0x3FCFFFFFF in internal RAM. To improve data transfer efficiency, GDMA can send data in burst mode, which is disabled by default. This mode is enabled for receive channels by setting GDMA_IN_DATA_BURST_EN_CHn, and enabled for transmit channels by setting GDMA_OUT_DATA_BURST_EN_CHn.

Table 2.4-2. Descriptor Field Alignment Requirements

| Inlink/Outlink | Burst Mode | Size       | Length | Buffer Address Pointer |
|----------------|------------|------------|--------|-------------------------|
| Inlink         | 0          | —          | —      | —                       |
|                | 1          | Word-aligned | —      | Word-aligned            |
| Outlink        | 0          | —          | —      | —                       |
|                | 1          | —          | —      | —                       |
```