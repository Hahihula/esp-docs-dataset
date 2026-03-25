

```markdown
| Data Mode | CMD State | Address State | Data State |
|-----------|-----------|---------------|------------|
| 1-bit SPI | 1-bit     | 1-bit         | 1-bit      |
| Dual SPI  | Dual Output Read | 1-bit       | 1-bit      |
|           | Dual I/O Read    | 1-bit       | 2-bit      |
| Quad SPI  | Quad Output Read | 1-bit       | 1-bit      |
|           | Quad I/O Read    | 1-bit       | 4-bit      |
| QPI       | 4-bit     | 4-bit         | 4-bit      |

Table 26.5-1. Data Modes Supported by GP-SPI2

For more information about the states used when GP-SPI2 works as a master or a slave, see Section 26.5.9 and Section 26.5.10, respectively.

26.5.2 FSPI Bus Signals
Table 26.5-2 describes the functions of FSPI bus signals. Table 26.5-3 lists the signals used in various SPI modes.

Table 26.5-2. Functional Description of FSPI Bus Signals

| FSPI Bus Signal | Function                                                                 |
|-----------------|---------------------------------------------------------------------------|
| FSPID           | MOSI/SIOO (serial data input and output, bit0)                           |
| FSPIQ           | MISO/SIO1 (serial data input and output, bit1)                           |
| FSPIWP          | SIO2 (serial data input and output, bit2)                                |
| FSPIDHD         | SIO3 (serial data input and output, bit3)                                |
| FSPICLK         | Input and output clock as master/slave                                   |
| FSPICSO         | Input and output CS signal as master/slave                               |
| FSPICS1~5       | Output CS signal as master                                               |
```