

```markdown
| FSPI Bus Signal | FD¹ | 1-bit SPI (3-line HD², 4-line HD) | Master |       |       |       | Slave |      |      |
|-----------------|-----|------------------------------------|--------|-------|-------|-------|-------|------|------|
|                 |     |                                    |        | 2-bit Dual SPI | 4-bit Quad SPI | QPI   |       | 1-bit SPI (3-line HD, 4-line HD) |      |
|                 |     |                                    |        |                |               |       | FD    |                            |      |
| FSPICLK         | Y   | Y                                  | Y      | Y               | Y             | Y     | Y     | Y                          | Y    |
| FSPICS0         | Y   | Y                                  | Y      | Y               | Y             | Y     | Y     | Y                          | Y    |
| FSPICS1         | Y   | Y                                  | Y      | Y               | Y             |       |       |                            |      |
| FSPICS2         | Y   | Y                                  | Y      | Y               | Y             | Y     |       |                            |      |
| FSPICS3         | Y   | Y                                  | Y      | Y               | Y             | Y     |       |                            |      |
| FSPICS4         | Y   | Y                                  | Y      | Y               | Y             | Y     |       |                            |      |
| FSPICS5         | Y   | Y                                  | Y      | Y               | Y             | Y     |       |                            |      |
| FSPID           | Y   | Y (Y)³                             |        | Y⁴               | Y⁵            | Y     | Y     | (Y)⁶                        | Y⁷   |
| FSPIQ           | Y   | (Y)³                               |        | Y⁴               | Y⁵            | Y     |       | (Y)⁶                        | Y⁷   |
| FSPWIP          |     |                                   |        |                 | Y⁵            | Y     |       |                            | Y⁸   |
| FSPIHD          |     |                                   |        |                 | Y⁵            | Y     |       |                            | Y⁸   |

¹ FD: full-duplex
² HD: half-duplex
³ Only one of the two signals is used at a time.
⁴ The two signals are used in parallel.
⁵ The four signals are used in parallel.
⁶ Only one of the two signals is used at a time.
⁷ The two signals are used in parallel.
⁸ The four signals are used in parallel.
```