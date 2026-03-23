

```markdown
## Table 27.5-1. Data Modes Supported by GP-SPI2

| Supported Mode | CMD State | Address State | Data State |
|----------------|-----------|---------------|------------|
| 1-bit SPI      | 1-bit     | 1-bit         | 1-bit      |
| Dual SPI       | 1-bit     | 1-bit         | 2-bit      |
|                |           | 2-bit         | 2-bit      |
| Quad SPI       | 1-bit     | 1-bit         | 4-bit      |
|                |           | 4-bit         | 4-bit      |
| QPI            | 4-bit     | 4-bit         | 4-bit      |

## Table 27.5-2. Mapping of FSPI Bus Signals

<table><thead><tr><th colspan="2">Standard SPI Protocol</th><th rowspan="2">Extended SPI Protocol<br>FSPI Bus Signal</th></tr><tr><th>Full-Duplex<br>SPI Signal</th><th>Half-Duplex<br>SPI Signal</th></tr></thead><tbody><tr><td>MOSI</td><td>MOSI</td><td>FSPID</td></tr><tr><td>MISO</td><td>(MISO)</td><td>FSPIQ</td></tr><tr><td>CS</td><td>CS</td><td>FSPICSO ~ 5</td></tr><tr><td>CLK</td><td>CLK</td><td>FSPICLK</td></tr><tr><td>-</td><td>-</td><td>FSPIWP</td></tr><tr><td>-</td><td>-</td><td>FSPIHD</td></tr></tbody></table>

## Table 27.5-3. Functional Description of FSPI Bus Signals

<table><thead><tr><th>FSPI Bus Signal</th><th>Function</th></tr></thead><tbody><tr><td>FSPID</td><td>MOSI/SIOO (serial data input and output, bit0)</td></tr><tr><td>FSPIQ</td><td>MISO/SIO1 (serial data input and output, bit1)</td></tr><tr><td>FSPIWP</td><td>SIO2 (serial data input and output, bit2)</td></tr><tr><td>FSPIDHD</td><td>SIO3 (serial data input and output, bit3)</td></tr></tbody></table>
```