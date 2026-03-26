

```markdown
| LP_SPI_WK_SLV_CHAR_NUM | LP_SPI_SLV_WK_MASK | Character Sequence |
|-------------------------|--------------------|--------------------|
| 1                       | 0xF                | CHAR4              |
| 2                       | 0x7                | CHAR3/CHAR4        |
| 3                       | 0x3                | CHAR2/CHAR3/CHAR4  |
| 4                       | 0x1                | CHAR1/CHAR2/CHAR3/CHAR4 |
| 5                       | 0x0                | CHAR0/CHAR1/CHAR2/CHAR3/CHAR4 |
```

## 43.10 Differences Among LP-SPI, GP-SPI2, and GP-SPI3

### 43.10.1 Feature Differences

Table 43.10-1 lists the differences among GP-SPI2, GP-SPI3, and LP-SPI on their supported features.

Table 43.10-1. Feature Differences Among GP-SPI2, GP-SPI3, and LP-SPI

| Feature                                                                 | GP-SPI2       | GP-SPI3        | LP-SPI         |
|-------------------------------------------------------------------------|---------------|----------------|----------------|
| Data modes supported in CMD/ADDR/DOUT/DIN states when working as a master | 1/2/4/8-bit   | 1/2/4-bit      | 1-bit          |
| Data modes supported in CMD/ADDR/DOUT/DIN states when working as a slave | 1/2/4-bit     | 1/2/4-bit      | 1-bit          |
| DMA-controlled transfers                                               | Support all DMA-controlled transfers | Not support DMA-controlled configurable segmented transfer | Not support any DMA related transfers |
| I/O mapping                                                             | Via HP GPIO matrix or HP IO MUX | Via HP GPIO matrix | Via LP GPIO matrix or LP IO MUX |
| CS line amount                                                          | 6             | 3              | 1              |
| Unaligned byte transfer                                                 | Support       | Support        | Not support    |
| DTR feature                                                             | Support       | Not support    | Not support    |

cont'd on next page
```