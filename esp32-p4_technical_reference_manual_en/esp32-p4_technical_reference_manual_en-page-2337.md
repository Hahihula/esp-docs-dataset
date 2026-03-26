

```markdown
Register 43.84. LP_SPI_MISC_REG (0x0020)

| Bit | Name                     | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)               |                                                                             |
| 30  | LP_SPI_CS_KEEP_ACTIVE    | Configures whether or not to keep the SPI_CS line low.                      |
|     |                          | 0: Not keep low                                                             |
|     |                          | 1: Keep low                                                                 |
|     | (R/W)                    |                                                                             |
| 29  | LP_SPI_CS_KEEP_ACTIVE    |                                                                             |
| 28  | LP_SPI_CS_KEEP_ACTIVE    |                                                                             |
| 27  | LP_SPI_CS_KEEP_ACTIVE    |                                                                             |
| 26  | LP_SPI_CS_KEEP_ACTIVE    |                                                                             |
| 25  | LP_SPI_CS_KEEP_ACTIVE    |                                                                             |
| 24  | (reserved)               |                                                                             |
| 23  | LP_SPI_SLAVE_CS_POL      | Configures whether or not invert SPI slave input CS polarity.                |
|     |                          | 0: Not change                                                               |
|     |                          | 1: Invert                                                                    |
|     | (R/W)                    |                                                                             |
| 22  | LP_SPI_SLAVE_CS_POL      |                                                                             |
| 21  | LP_SPI_SLAVE_CS_POL      |                                                                             |
| 20  | LP_SPI_SLAVE_CS_POL      |                                                                             |
| 19  | LP_SPI_SLAVE_CS_POL      |                                                                             |
| 18  | (reserved)               |                                                                             |
| 17  | LP_SPI_MASTER_CS_POL     | Configures the polarity of SPI_CSO line in master transfer.                  |
|     |                          | 0: SPI_CSO is low active.                                                   |
|     |                          | 1: SPI_CSO is high active.                                                  |
|     | (R/W)                    |                                                                             |
| 16  | LP_SPI_MASTER_CS_POL     |                                                                             |
| 15  | LP_SPI_MASTER_CS_POL     |                                                                             |
| 14  | LP_SPI_MASTER_CS_POL     |                                                                             |
| 13  | LP_SPI_MASTER_CS_POL     |                                                                             |
| 12  | (reserved)               |                                                                             |
| 11  | LP_SPI_CLK_DIS           | Configures whether or not to disable SPI_CLK output.                         |
|     |                          | 0: Enable                                                                   |
|     |                          | 1: Disable                                                                  |
|     | (R/W)                    |                                                                             |
| 10  | LP_SPI_CLK_DIS           |                                                                             |
| 9   | LP_SPI_CLK_DIS           |                                                                             |
| 8   | LP_SPI_CLK_DIS           |                                                                             |
| 7   | (reserved)               |                                                                             |
| 6   | LP_SPI_SLOE_DIS          | Configures whether or not to disable SPI_CS pin.                             |
|     |                          | 0: SPI_CSO signal is from/to SPI_CSO pin                                    |
|     |                          | 1: Disable SPI_CSO pin                                                      |
|     | (R/W)                    |                                                                             |
| 5   | LP_SPI_SLOE_DIS          |                                                                             |
| 4   | LP_SPI_SLOE_DIS          |                                                                             |
| 3   | LP_SPI_SLOE_DIS          |                                                                             |
| 2   | LP_SPI_SLOE_DIS          |                                                                             |
| 1   | (reserved)               |                                                                             |
| 0   | Reset                    |                                                                             |

LP_SPI_CSO_DIS Configures whether or not to disable SPI_CSO pin.
0: SPI_CSO signal is from/to SPI_CSO pin.
1: Disable SPI_CSO pin.
(R/W)

LP_SPI_CLK_DIS Configures whether or not to disable SPI_CLK output.
0: Enable
1: Disable
(R/W)

LP_SPI_MASTER_CS_POL Configures the polarity of SPI_CSO line in master transfer.
0: SPI_CSO is low active.
1: SPI_CSO is high active.
(R/W)

LP_SPI_SLAVE_CS_POL Configures whether or not invert SPI slave input CS polarity.
0: Not change
1: Invert
(R/W)

LP_SPI_CLK_IDLE_EDGE Configures the level of SPI_CLK line when LP-SPI is in idle.
0: Low
1: High
(R/W)
```