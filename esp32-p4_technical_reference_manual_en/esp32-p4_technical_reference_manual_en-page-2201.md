
```markdown
## 43.5 Functional Description

### 43.5.1 Data Modes

GP-SPI and LP-SPI can be configured as either a master or a slave to communicate with other SPI devices in the following data modes, see Table 43.5-1. For more information about the data modes used when GP-SPI or LP-SPI works as a master, see Section 43.5.9, and Section 43.5.10 for GP-SPI working as a slave.

Table 43.5-1. Data Modes Supported by GP-SPI and LP-SPI

| Data Mode | CMD State | Address State | Data State | GP-SPI2 | GP-SPI3 | LP-SPI |
|-----------|-----------|---------------|------------|---------|---------|--------|
| 1-bit SPI | 1-bit     | 1-bit         | 1-bit      | Y       | Y       | Y      |
| Dual SPI  | 1-bit     | 1-bit         | 2-bit      | Y       | Y       | —      |
|           |           | 2-bit         | 2-bit      | Y       | Y       | —      |
| Quad SPI  | 1-bit     | 1-bit         | 4-bit      | Y       | Y       | —      |
|           |           | 4-bit         | 4-bit      | Y       | Y       | —      |
| Octal SPI | 1-bit     | 1-bit         | 8-bit      | Y       | —       | —      |
|           |           | 8-bit         | 8-bit      | Y       | —       | —      |
| QPI       | 4-bit     | 4-bit         | 4-bit      | Y       | Y       | —      |
| OPI       | 8-bit     | 8-bit         | 8-bit      | Y       | —       | —      |

### 43.5.2 Introduction to Bus Signals

The functional description of SPI2/SPI3 and LP_SPI bus signals is shown in Table 43.5-2. Tables 43.5-3, 43.5-4, and 43.5-5 list the signals used in various SPI modes.

Table 43.5-2. Functional Description of SPI2/SPI3 and LP_SPI Bus Signals

| SPI2 Bus Signal | SPI3 Bus Signal | LP-SPI Bus Signal | Function |
|-----------------|-----------------|-------------------|----------|
| SPI2CLK         | SPI3_CLK        | LP_SPI_CLK        | Input and output clock as master/slave |
| SPI2CS0         | SPI3_CS0        | LP_SPI_CS         | Input and output CS signal as master/slave |
| SPI2CS1 ~5      | SPI3_CS1~5      | —                 | Output CS signal as master |
| SPI2D           | SPI3_D          | LP_SPI_D          | MOSI/SIO0 (serial data input and output, bit0) |
| SPI2Q           | SPI3_Q          | LP_SPI_Q          | MISO/SIO1 (serial data input and output, bit1) |
| SPI2WP          | SPI3_WP         | —                 | SIO2 (serial data input and output, bit2) |
| SPI2HD          | SPI3_HD         | —                 | SIO3 (serial data input and output, bit3) |
| SPI2D4~7        | —               | —                 | SI04~7 (serial data input and output, bit4~7) |
| SPI2DQS         | —               | —                 | Output data mask signal as master |
```