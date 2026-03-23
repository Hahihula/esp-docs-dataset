

```markdown
or PARLIO, the GDMA controller also supports GDMA_IN_ERR_CHn_EOF_INT interrupt. This interrupt is enabled by setting `GDMA_IN_ERR_EOF_CHn_INT_ENA` bit, and it indicates that a data segment corresponding to a descriptor has been received with errors.

When detecting a GDMA_OUT_TOTAL_EOF_CHn_INT or a GDMA_IN_SUC_EOF_CHn_INT interrupt, software can record the value of `GDMA_OUT_EOF_DES_ADDR_CHn` or `GDMA_IN_SUC_EOF_DES_ADDR_CHn` field, i.e. address of the last descriptor. Therefore, software can tell which descriptors have been used and reclaim them as needed.

**Note:** In this chapter, EOF of transmit descriptors refers to `suc_eof`, while EOF of receive descriptors refers to both `suc_eof` and `err_eof`.

## 4.4.7 Accessing Internal RAM

Any transmit and receive channels of GDMA can access `0x40800000 ~ 0x4087FFFF` in internal RAM. To improve data transfer efficiency, GDMA can send data in burst mode, which is disabled by default. This mode is enabled for receive channels by setting `GDMA_IN_DATA_BURST_EN_CHn`, and enabled for transmit channels by setting `GDMA_OUT_DATA_BURST_EN_CHn`.

**Table 4.4-2. Descriptor Field Alignment Requirements**

<table><thead><tr><th>Inlink/Outlink</th><th>Burst Mode</th><th>Size</th><th>Length</th><th>Buffer Address Pointer</th></tr></thead><tbody><tr><td rowspan="2">Inlink</td><td>O</td><td>—</td><td>—</td><td>—</td></tr><tr><td>1</td><td>Word-aligned</td><td>—</td><td>Word-aligned</td></tr><tr><td rowspan="2">Outlink</td><td>O</td><td>—</td><td>—</td><td>—</td></tr><tr><td>1</td><td>—</td><td>—</td><td>—</td></tr></tbody></table>

Table 4.4-2 lists the requirements for descriptor field alignment when accessing internal RAM.

When burst mode is disabled, size, length, and buffer address pointer in both transmit and receive descriptors do not need to be word-aligned. That is, for a descriptor, GDMA can read data of specified length (1 ~ 4095 bytes) from any start addresses in the accessible address range, or write received data of the specified length (1 ~ 4095 bytes) to any contiguous addresses in the accessible address range.

When burst mode is enabled, size, length, and buffer address pointer in transmit descriptors are also not necessarily word-aligned. However, size and buffer address pointer in receive descriptors except length should be word-aligned.

## 4.4.8 Arbitration

To ensure timely response to peripherals running at a high speed with low latency (such as SPI), the GDMA controller implements a fixed-priority channel arbitration scheme. That is to say, each channel can be assigned a priority from 0 ~ 5 (in total 6 levels). The larger the number, the higher the priority, and the more timely the response. When several channels are assigned the same priority, the GDMA controller adopts a round-robin arbitration scheme.

## 4.4.9 Event Task Matrix Feature

The GDMA controller on ESP32-C6 supports the Event Task Matrix (ETM) function, which allows GDMA's ETM tasks to be triggered by any peripherals' ETM events, or GDMA's ETM events to trigger any peripherals' ETM
```