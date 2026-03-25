

```markdown
| Inlink/Outlink | Burst Mode | Size          | Length | Buffer Address Pointer |
|----------------|------------|---------------|--------|-------------------------|
|                |            |               |        |                         |
| Inlink         | 0          | —             | —      | —                       |
|                |            | Word-aligned   | —      | Word-aligned            |
| Outlink        | 0          | —             | —      | —                       |
|                |            | —             | —      |                         |

Table 3.4-2. Descriptor Field Alignment Requirements
```

```markdown
## 3.4.7 Accessing Internal RAM

Any transmit and receive channels of GDMA can access `0x40800000 ~ 0x4084FFFF` in internal RAM. To improve data transfer efficiency, GDMA can send data in burst mode, which is disabled by default. This mode is enabled for receive channels by setting `GDMA_IN_DATA_BURST_EN_CHn`, and enabled for transmit channels by setting `GDMA_OUT_DATA_BURST_EN_CHn`.

## 3.4.8 Arbitration

To ensure timely response to peripherals running at a high speed with low latency (such as SPI), the GDMA controller implements a fixed-priority channel arbitration scheme. That is to say, each channel can be assigned a priority from `0 ~ 5` (in total 6 levels). The larger the number, the higher the priority, and the more timely the response. When several channels are assigned the same priority, the GDMA controller adopts a round-robin arbitration scheme.

## 3.4.9 Event Task Matrix Feature

The GDMA controller on ESP32-H2 supports the Event Task Matrix (ETM) function, which allows GDMA’s ETM tasks to be triggered by any peripherals’ ETM events, or GDMA’s ETM events to trigger any peripherals’ ETM
```