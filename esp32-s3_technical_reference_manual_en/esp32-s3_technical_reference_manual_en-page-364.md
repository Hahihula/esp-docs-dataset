**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Body Text:**

by setting `GDMA_IN_ERR_EOF_CHn_INT_ENA` bit, and it indicates that a data segment corresponding to a descriptor has been received with errors.

When detecting a `GDMA_OUT_TOTAL_EOF_CHn_INT` or a `GDMA_IN_SUC_EOF_CHn_INT` interrupt, software can record the value of `GDMA_OUT EDUC_DES_ADDR_CHn` or `GDMA_IN_SUC_EOF EDUC_DES_ADDR_CHn` field, i.e., address of the last descriptor. Therefore, software can tell which descriptors have been used and reclaim them.

**Note:**
In this chapter, EOF of transmit descriptors refers to suc_eof, while EOF of receive descriptors refers to both suc_eof and err_eof.

**Subsection Title: 3.4.8 Accessing Internal RAM**

Any transmit and receive channels of GDMA can access `0x3FC88000 ~ 0x3FFFFF` in internal RAM. To improve data transfer efficiency, GDMA can send data in burst mode, which is disabled by default. This mode is enabled for receive channels by setting `GDMA_IN DATA BURST_EN CHn`, and enabled for transmit channels by setting `GDMA_OUT DATA BURST_EN CHn`.

**Table Title: Table 3.4-2. Descriptor Field Alignment Requirements for Accessing Internal RAM**

| Inlink/Outlink | Burst Mode | Size       | Length   | Buffer Address Pointer |
|-----------------|------------|------------|----------|-----------------------|
| Inlink          | O          | —          | —        | Word-aligned          |
| Outlink         |            | Word-aligned | —       |                       |

**Body Text:**

Table 3.4-2 lists the requirements for descriptor field alignment when GDMA accesses internal RAM.

When burst mode is disabled, size, length, and buffer address pointer in both transmit and receive descriptors do not need to be word-aligned. That is to say, GDMA can read data of specified length (1 ~ 4095 bytes) from any start addresses in the accessible address range, or write received data of the specified length (1 ~ 4095 bytes) to any contiguous addresses in the accessible address range.

When burst mode is enabled, size, length, and buffer address pointer in transmit descriptors are also not necessarily word-aligned. However, size and buffer address pointer in receive descriptors except length should be word-aligned.

**Subsection Title: 3.4.9 Accessing External RAM**

Any transmit and receive channels of GDMA can access `0x3C000000 ~ 0x3FFFFFFF` in external RAM. GDMA can send data only in burst mode The number of data bytes to transfer in one burst is defined as block size. Block size can be 16 bytes, 32 bytes or 64 bytes, configured via `GDMA_IN EXT MEM BK SIZE CHn` for transmit channels and `GDMA_OUT EXT MEM BK SIZE CHn` for receive channels.

**Table Title: Table 3.4-3. Descriptor Field Alignment Requirements for Accessing External RAM**

| Inlink/Outlink | Size       | Length   | Buffer Address Pointer |
|----------------|------------|----------|-----------------------|
| Inlink          | Block-aligned | —        | Block-aligned         |
| Outlink         |            | —        |                       |

**Footer:**
Espressif Systems
364 ESP32-S3 TRM (Version 1.7)