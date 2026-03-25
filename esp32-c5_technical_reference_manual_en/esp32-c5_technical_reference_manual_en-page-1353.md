

```markdown
Register 37.3. USB_SERIAL_JTAG_CONFO_REG (0x0018)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | USB_SERIAL_JTAG_EXCHG_PINS_OVERRIDE       | Configures whether to enable software control USB D+ D- exchange.           |
|     |                                            | 0: Disable                                                                   |
|     |                                            | 1: Enable                                                                    |
|     | (R/W)                                     |                                                                             |
| 29  | USB_SERIAL_JTAG_EXCHG_PINS                | Configures whether to enable USB D+ D- exchange.                            |
|     |                                            | 0: Disable                                                                   |
|     |                                            | 1: Enable                                                                    |
|     | (R/W)                                     |                                                                             |
| 28  | USB_SERIAL_JTAG_VREFH                     | Configures single-end input high threshold.                                 |
|     |                                            | 0: 1.76 V                                                                    |
|     |                                            | 1: 1.84 V                                                                    |
|     |                                            | 2: 1.92 V                                                                    |
|     |                                            | 3: 2.00 V                                                                    |
|     | (R/W)                                     |                                                                             |
| 27  | USB_SERIAL_JTAG_VREFL                     | Configures single-end input low threshold.                                  |
|     |                                            | 0: 0.80 V                                                                    |
|     |                                            | 1: 0.88 V                                                                    |
|     |                                            | 2: 0.96 V                                                                    |
|     |                                            | 3: 1.04 V                                                                    |
|     | (R/W)                                     |                                                                             |
| 26  | USB_SERIAL_JTAG_VREF_OVERRIDE             | Configures whether to enable software control input threshold.              |
|     |                                            | 0: Disable                                                                   |
|     |                                            | 1: Enable                                                                    |
|     | (R/W)                                     |                                                                             |
```
Continued on the next page...
```