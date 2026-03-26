

```markdown
Register 36.3. ISP_CNTL_REG (0x0008)

| Bit | 31       | 30       | 29        | 28      | 27     | 26   | 25    | 24         | 23          | 22           | 21            | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----------|----------|-----------|---------|--------|------|-------|------------|-------------|--------------|---------------|----|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|     | ISP_OUT_TYPE | ISP_IN_SRC | ISP_DATA_TYPE | ISP_BYTE_ENDIAN_ORDER | (reserved) | ISP_WBG_EN | ISP_CROP_EN | ISP_HIST_EN | ISP_AWB_EN | ISP_AF_EN | ISP_AE_EN | ISP_SHARPEN_EN | ISP_RGBYV_COM_EN | ISP_GAMMA_EN | (reserved) | ISP_DEMOSAIC_EN | ISP_LSC_EN | ISP_BF_EN | ISP_DPC_EN | ISP_BLC_EN | ISP_MIPI_DATA_EN |
| 31  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 30  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 29  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 28  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 27  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 26  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 25  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 24  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 23  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 22  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 21  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 20  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 19  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 18  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 17  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 16  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 15  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 14  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 13  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 12  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 11  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 10  |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 9   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 8   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 7   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 6   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 5   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 4   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 3   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 2   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 1   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| 0   |           |           |             |                         |            |          |          |            |            |            |              |               |                |             |             |                 |           |         |        |       |       |       |      |     |    |   |   |   |   |   |   |
| Reset | 0x2 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 |
```

ISP_MIPI_DATA_EN Configures whether to enable the MIPI Image Interface 32 input.
- O: Disable
- 1: Enable (R/W)

ISP_EN Configures whether to enable the ISP.
- O: Disable
- 1: Enable (R/W)

ISP_BLC_EN Configures whether to enable the BLC module.
- O: Disable
- 1: Enable (R/W)

ISP_DPC_EN Configures whether to enable the DPC module.
- O: Disable
- 1: Enable (R/W)

ISP_BF_EN Configures whether to enable the BF module.
- O: Disable
- 1: Enable (R/W)

ISP_LSC_EN Configures whether to enable the LSC module.
- O: Disable
- 1: Enable (R/W)

ISP_DEMOSAIC_EN Configures whether to enable the demosaic module.
- O: Disable
- 1: Enable (R/W)

ISP_CCM_EN Configures whether to enable the CCM module.
- O: Disable
- 1: Enable (R/W)
```