

```markdown
| Bus Signal | SPI2 FD¹ | 3-line HD² | 4-line HD | Dual SPI | Quad SPI | QPI | Octal SPI | OPI | Slave FD | 1-bit HD | 3-line HD | 4-line HD | Dual SPI | Quad SPI | QPI |
|------------|----------|------------|-----------|----------|----------|-----|-----------|-----|----------|----------|-----------|-----------|----------|----------|-----|
|            |          |            |           | Master   |          |     |           |     |          | 1-bit SPI |           |           |          |         |      |
| SPI2CLK    | Y        | Y          | Y         | Y        | Y        | Y   | Y         | Y   | Y        | Y        | Y         | Y         | Y        | Y       | Y    |
| SPI2CS0    | Y        | Y          | Y         | Y        | Y        | Y   | Y         | Y   | Y        | Y        | Y         | Y         | Y        | Y       | Y    |
| SPI2CS1    | Y        | Y          | Y         | Y        | Y        | Y   | Y         |     |           |          |           |           |          |         |      |
| SPI2CS2    | Y        | Y          | Y         | Y        | Y        | Y   | Y         |     |           |          |           |           |          |         |      |
| SPI2CS3    | Y        | Y          | Y         | Y        | Y        | Y   | Y         |     |           |          |           |           |          |         |      |
| SPI2CS4    | Y        | Y          | Y         | Y        | Y        | Y   | Y         |     |           |          |           |           |          |         |      |
| SPI2CS5    | Y        | Y          | Y         | Y        | Y        | Y   | Y         |     |           |          |           |           |          |         |      |
| SPI2D      | Y        | (Y)³       | Y⁴        |          | Y⁵       | Y   | Y         | Y   | (Y)⁶     | (Y)⁷     |           |           |          |         |      |
| SPI2Q      | Y        | (Y)³       | Y⁴        |          | Y⁵       | Y   | Y         | Y   | (Y)⁶     | (Y)⁷     |           |           |          |         |      |
| SPI2WP     |          |            |           |          | Y⁵       | Y   | Y         |     |          |          |           |           |          |         |      |
| SPI2HD     |          |            |           |          | Y⁵       | Y   | Y         |     |          |          |           |           |          | Y⁸      | Y    |
| SPI2D4~7   |          |            |           |          |          |     | Y         | Y   |          |          |           |           |          |         |      |
| SPI2DQS    |          |            |           |          |          |     | Y         | Y   |          |          |           |           |          |         |      |

```