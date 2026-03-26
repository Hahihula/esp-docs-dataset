

```markdown
| Signal | SPI3 Bus Signal | Master |          |          | Slave |      |      |
|--------|-----------------|--------|----------|----------|-------|------|------|
|        |                 | FD¹    | 1-bit SPI |          | Dual SPI | Quad SPI | QPI   |
|        |                 | 3-line HD² | 4-line HD |          |         |         |       |
|        |                 |         |          |          |         |         |       |
| SPI3_CLK | Y               | Y      | Y        | Y        | Y      | Y      | Y     |
| SPI3_CSO | Y               | Y      | Y        | Y        | Y      | Y      | Y     |
| SPI3_CS1 | Y               | Y      | Y        | Y        | Y      |         |       |
| SPI3_CS2 | Y               | Y      | Y        | Y        | Y      | Y      |       |
| SPI3_D  | Y               | Y      | (Y)³     | γ⁴       | γ⁵     | Y      | γ⁶    |
| SPI3_Q  | Y               |         | (Y)³     | γ⁴       | γ⁵     | Y      | (Y)⁶  |
| SPI3_WP |                 |         |          |           | γ⁵     | Y      | γ⁸    |
| SPI3_HD |                 |         |          |           | γ⁵     | Y      | γ⁸    |

1 FD: full-duplex
2 HD: half-duplex
3 Only one of the two signals is used at a time.
4 The two signals are used in parallel.
5 The four signals are used in parallel.
6 Only one of the two signals is used at a time.
7 The two signals are used in parallel.
8 The four signals are used in parallel.
```