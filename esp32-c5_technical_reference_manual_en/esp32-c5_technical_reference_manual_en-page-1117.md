

```markdown
| Bit Mode | FSPI Bus Data   | SPI_RD/WR_BIT_ORDER = 0 (MSB) | SPI_RD/WR_BIT_ORDER = 2 (MSB) | SPI_RD/WR_BIT_ORDER = 1 (LSB) | SPI_RD/WR_BIT_ORDER = 3 (LSB) |
|----------|-----------------|-------------------------------|--------------------------------|--------------------------------|--------------------------------|
| 1-bit mode | FSPID or FSPIQ   | B7→B6→B5→B4→B3→B2→B1→B0       | B7→B6→B5→B4→B3→B2→B1→B0        | BO→B1→B2→B3→B4→B5→B6→B7         | BO→B1→B2→B3→B4→B5→B6→B7         |
| 2-bit mode | FSPIQ           | B7→B5→B3→B1                   | B6→B4→B2→B0                    | B1→B3→B5→B7                     | BO→B2→B4→B6                     |
|          | FSPID           | B6→B4→B2→B0                   | B7→B5→B3→B1                    | BO→B2→B4→B6                     | B1→B3→B5→B7                     |
| 4-bit mode | FSPIHD          | B7→B3                         | B4→B0                          | B3→B7                           | B0→B4                           |
|          | FSPIWP          | B6→B2                         | B5→B1                          | B2→B6                           | B1→B5                           |
|          | FSPIQ           | B5→B1                         | B6→B2                          | B1→B5                           | B2→B6                           |
|          | FSPID           | B4→B0                         | B7→B3                          | B0→B4                           | B3→B7                           |
```