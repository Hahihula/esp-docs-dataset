

```markdown
| Espressif Signals | FSPI Signal | FD¹ | 1-bit SPI 3-line HD² | 4-line HD | Master 2-bit Dual SPI | 4-bit Quad SPI | QPI | FD | 1-bit SPI 3-line HD | 4-line HD | Slave 2-bit Dual SPI | 4-bit Quad SPI | QPI |
|-------------------|-------------|-----|----------------------|-----------|------------------------|-----------------|-----|----|---------------------|-----------|-----------------------|-----------------|-----|
|                   |             |     |                      |           |                        |                 |     |    |                     |           |                       |                 |     |
| FSPICLK           | Y           | Y   | Y                    | Y         | Y                      | Y               | Y   | Y  | Y                   | Y         | Y                     | Y               | Y   |
| FSPICS0           | Y           | Y   | Y                    | Y         | Y                      | Y               | Y   | Y  | Y                   | Y         | Y                     | Y               | Y   |
| FSPICS1           | Y           | Y   | Y                    | Y         | Y                      | Y               |     |    |                     |           |                       |                 |     |
| FSPICS2           | Y           | Y   | Y                    | Y         | Y                      | Y               |     |    |                     |           |                       |                 |     |
| FSPICS3           | Y           | Y   | Y                    | Y         | Y                      | Y               | Y   |    |                     |           |                       |                 |     |
| FSPICS4           | Y           | Y   | Y                    | Y         | Y                      | Y               | Y   |    |                     |           |                       |                 |     |
| FSPICS5           | Y           | Y   | Y                    | Y         | Y                      | Y               | Y   |    |                     |           |                       |                 |     |
| FSPID             | Y           | Y   | (Y)³                 |            | γ⁴                     | γ⁵              | Y   | Y  |                     | (γ)⁶      | γ⁷                     | γ⁸               | Y   |
| FSPIQ             | Y           |     | (Y)³                 |            | γ⁴                     | γ⁵              | Y   | Y  |                     | (γ)⁶      | γ⁷                     | γ⁸               | Y   |
| FSPIWP            |             |     |                      |           |                        | γ⁵              | Y   |    |                     |           |                       |                 |     |
| FSPIDHD           |             |     |                      |           |                        | γ⁵              | Y   |    |                     |           |                       |                 |     |

1 FD: full-duplex
2 HD: half-duplex
3 Only one of the two signals is used at a time.
4 The two signals are used in parallel.
5 The four signals are used in parallel.
6 Only one of the two signals is used at a time.
7 The two signals are used in parallel.
8 The four signals are used in parallel.
```