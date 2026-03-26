

```markdown
| Bit Mode | SPI2 Bus Data | SPI_RD/WR_BIT_ORDER = 0 (MSB) | SPI_RD/WR_BIT_ORDER = 2 (MSB) | SPI_RD/WR_BIT_ORDER = 1 (LSB) | SPI_RD/WR_BIT_ORDER = 3 (LSB) |
|----------|---------------|-------------------------------|--------------------------------|--------------------------------|--------------------------------|
| 1-bit mode | SPI2D or SPI2Q | B7→B6→B5→B4→B3→B2→B1→B0 | B7→B6→B5→B4→B3→B2→B1→B0 | B0→B1→B2→B3→B4→B5→B6→B7 | B0→B1→B2→B3→B4→B5→B6→B7 |
| 2-bit mode | SPI2Q         | B7→B5→B3→B1                   | B6→B4→B2→B0                   | B1→B3→B5→B7                   | B0→B2→B4→B6                   |
|          | SPI2D         | B6→B4→B2→B0                   | B7→B5→B3→B1                   | B0→B2→B4→B6                   | B1→B3→B5→B7                   |
| 4-bit mode | SPI2HD        | B7→B3                         | B4→B0                         | B3→B7                         | B0→B4                         |
|          | SPI2WP        | B6→B2                         | B5→B1                         | B2→B6                         | B1→B5                         |
|          | SPI2Q         | B5→B1                         | B6→B2                         | B1→B5                         | B2→B6                         |
|          | SPI2D         | B4→B0                         | B7→B3                         | B0→B4                         | B3→B7                         |
|          | SPI2D7        | B7                            | B7                            | B0                            | B0                            |
|          | SPI2D6        | B6                            | B6                            | B1                            | B1                            |
| 8-bit mode | SPI2D5        | B5                            | B5                            | B2                            | B2                            |
|          | SPI2D4        | B4                            | B4                            | B3                            | B3                            |
|          | SPI2HD        | B3                            | B3                            | B4                            | B4                            |
|          | SPI2WP        | B2                            | B2                            | B5                            | B5                            |
|          | SPI2Q         | B1                            | B1                            | B6                            | B6                            |
|          | SPI2D         | B0                            | B0                            | B7                            | B7                            |

Table 43.5-6. Bit Order Control in GP-SPI (Take GP-SPI2 as an Example)

Table 43.5-7. Bit Order Control in LP-SPI

| Bit Mode | LP_SPI Bus Signal | LP_SPI_RD/WR_BIT_ORDER = 0 (MSB) | LP_SPI_RD/WR_BIT_ORDER = 1 (LSB) |
|----------|-------------------|----------------------------------|----------------------------------|
| 1-bit mode | LP_SPI_D or LP_SPI_Q | B7→B6→B5→B4→B3→B2→B1→B0 | B0→B1→B2→B3→B4→B5→B6→B7 |
```