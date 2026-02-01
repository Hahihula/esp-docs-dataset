**Title:**
2 Pins

**Subtitle:**
2.3 IO Pins

**Subsection Title:**
2.3.1 IO MUX Functions

**Body Text:**
The IO MUX allows multiple input/output signals to be connected to a single input/output pin. Each IO pin of ESP32-H2 can be connected to one of the five signals (IO MUX functions, i.e., FO-F4), as listed in Table 2-3 IO MUX Pin Functions.

Among the five sets of signals:
- Some are routed via the GPIO Matrix (GPIO0, GPIO1, etc.), which incorporates internal signal routing circuitry for mapping signals programmatically. It gives the pin access to almost any peripheral signals. However, the flexibility of programmatic mapping comes at a cost as it might affect the latency of routed signals. For details about connecting to peripheral signals via GPIO Matrix, see ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.
- Some are directly routed from certain peripherals (UOTXD, MTCK, etc.), including UARTO, JTAG, and SPI2 - see Table 2-2 Peripheral Signals Routed via IO MUX.

**Table:**
- **Title:** Table 2-2. Peripheral Signals Routed via IO MUX
  | Pin Function | Signal       | Description |
  |--------------|-------------|-------------|
  | UOTXD        | Transmit data | UARTO interface |
  | UORXD        | Receive data |                 |
  | MTCK         | Test clock   |               |
  | MTDO         | Test Data Out | JTAG interface for debugging |
  | MTDI         | Test Data In  |             |
  | MTMS         | Test Mode Select |           |
  | FSPIQ        | Data out     |              |
  | FSPID        | Data in      |              |
  | FSPIHD       | Hold         | SPI2 interface for fast SPI connection. It supports 1-, 2-, 4-line SPI modes |
  | FSPIWP       | Write protect |                 |
  | FSMCLK       | Clock        |               |
  | FSPICS...    | Chip select  |              |

**Table:**
- **Title:** Table 3-2. IO MUX Pin Functions
  | Pin No. | IO MUX / GPIO Name | Type FO | Type F1 | Type F2 | Type F3 | Type F4 |
  |---------|--------------------|--------|--------|--------|--------|--------|
  | 3       | GPIO0              | I/O/T  | GPIO0  | FSPIQ  | I/O/T  | I/O/T  |
  | 4       | GPIO1              | I/O/T  | GPIO1  | FSPICSO| I/O/T  | I/O/T  |
  | 5       | MTMS               | II     | GPIO2  | FSPIWP | I/O/T  | I/O/T  |
  | 6       | GPIO3              | O/T    | GPIO3  | FSPIHD | I/O/T  | I/O/T  |
  | 7       | GPIO4              | I1     | GPIO4  | FSPICLK| I/O/T  | I/O/T  |
  | 8       | GPIO5              | II     | GPIO5  | FSPID  | I/O/T  | I/O/T  |
  | 9       | GPIO6              | O/T    | GPIO6  | FSPI   | I/O/T  | I/O/T  |
  | 10      | GPIO8              | I/O/T  | GPIO8  |        |        |        |

**Footer:**
Espressif Systems
ESP32-H2 Series Datasheet v1.2

**Note:** Submit Documentation Feedback