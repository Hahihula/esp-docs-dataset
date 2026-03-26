

```markdown
| Channel Valid Data Width | I2S_TX_BITS_MOD | I2S_TX_24_FILL_EN |
|--------------------------|-----------------|-------------------|
| 32                       | 31              | x*                |
|                          | 23              | 1                 |
| 24                       | 23              | 0                 |
| 16                       | 15              | x                 |
| 8                        | 7               | x                 |

\* "x" represents that this value is ignored.
```

### 46.9.1 Data Format Control

Data format is controlled in the following phases:

- Phase I: Read data from memory and write it to TX FIFO;
- Phase II: Read the TX data from TX FIFO and convert the data according to the output data mode;
- Phase III: Clock out the TX data serially.

#### 46.9.1.1 Bit Width Control of Channel Valid Data

The bit width of the valid data in each channel is determined by `I2S_TX_BITS_MOD` and `I2S_TX_24_FILL_EN`. For details, see the table below.

Table 46.9-1. Bit Width of Channel Valid Data

| Channel Valid Data Width | I2S_TX_BITS_MOD | I2S_TX_24_FILL_EN |
|--------------------------|-----------------|-------------------|
| 32                       | 31              | x*                |
|                          | 23              | 1                 |
| 24                       | 23              | 0                 |
| 16                       | 15              | x                 |
| 8                        | 7               | x                 |

\* "x" represents that this value is ignored.

#### 46.9.1.2 Endian Control of Channel Valid Data

When `I2S` reads data through GDMA, the data endian under various data width is controlled by `I2S_TX_BIG_ENDIAN`. Table 46.9-2 shows how `I2S_TX_BIG_ENDIAN` controls the reading of the data with different valid data widths of the channel.

Table 46.9-2. Endian of Channel Valid Data

| Channel Valid Data Width | Original Data   | Endian of Processed Data                     | I2S_TX_BIG_ENDIAN |
|--------------------------|-----------------|-----------------------------------------------|-------------------|
| 32                       | {B3, B2, B1, B0} | {B3, B2, B1, B0}                              | 0                 |
|                          |                 | {B0, B1, B2, B3}                             | 1                 |
| 24                       | {B2, B1, B0}    | {B2, B1, B0}                                  | 0                 |
|                          |                 | {B0, B1, B2}                                  | 1                 |
| 16                       | {B1, B0}        | {B1, B0}                                      | 0                 |
|                          |                 | {B0, B1}                                      | 1                 |
| 8                        | {B0}            | {B0}                                          | x                 |

**Note:**
B0, B1, B2, B3 each represents an 8-bit data, and the symbol {} indicates that the bytes are combined together. For
```