**Title:**
2 Pins

**Subtitle:**
2.3.2 LP IO MUX Functions

**Body Text:**
When the chip is in Deep-sleep mode, the IO MUX described in Section 2.3.1 IO MUX Functions will not work.
That is where the LP IO MUX comes in. It allows multiple input/output signals to be a single input/output pin in Deep-sleep mode, as the pin is connected to the LP system and powered by VDD_LP or VDD_BAT.

LP IO pins can be assigned to LP IO MUX functions. They can:
- Either work as LP GPIOs (LP_GPIO0, LP_GPIO1, etc.), connected to the LP CPU
- Or connect to LP peripheral signals (LP_UART_TXD_PAD, LP_UART_RXD_PAD) - see Table 2-4 LP IO MUX Functions

**Table Descriptions:**

**Table 2-4. LP Peripheral Signals Routed via LP IO MUX**
| Pin Function | Signal    | Description |
|---------------|-----------|-------------|
| LP_UART_TXD_PAD | Transmit data | LP UART interface |
| LP_UART_RXD_PAD | Receive data | |

**Table Descriptions:**

**Table 2-5. LP IO MUX Functions**
| Pin No. | LP IO Name | F0 Type | F1 Type |
|---------|-----------|--------|--------|
| 1       | LP_GPIO1   | I/O/T  | LP_LGPIO1 | I/O/T |
| 2       | LP_GPIO2   | I/O/T  | LP_LGPIO2 | I/O/T |
| ...     | ...       | ...    | ...      | ...    |

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version Information:**
ESP32-P4 Series Datasheet v0.6, Page 22