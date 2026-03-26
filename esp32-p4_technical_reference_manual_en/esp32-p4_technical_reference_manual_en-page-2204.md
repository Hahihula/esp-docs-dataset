

```markdown
| LP_SPI Bus Signal | FD¹ | Master (1-bit SPI)                     | Slave (1-bit SPI)               |
|-------------------|-----|----------------------------------------|----------------------------------|
|                   |     | 3-line HD²                             |                                  |
|                   |     | 4-line HD                              |                                  |
| LP_SPI_CLK        | Y   | Y                                      | Y                                |
| LP_SPI_CS         | Y   | Y                                      | Y                                |
| LP_SPI_D          | Y   | Y                                      | (Y)³                             |
| LP_SPI_Q          | Y   | (Y)³                                   | (Y)³                             |

¹ FD: full-duplex
² HD: half-duplex
³ Only one of the two signals is used at a time.
```

## 43.5.3 Bit Read/Write Order Control

* **GP-SPI**

    - When operating as a master:
        * The bit order of the command, address and data sent by the GP-SPI master is controlled by `SPI_WR_BIT_ORDER`.
        * The bit order of the data received by the master is controlled by `SPI_RD_BIT_ORDER`.

    - When operating as a slave:
        * The bit order of the data sent by the GP-SPI slave is controlled by `SPI_WR_BIT_ORDER`.
        * The bit order of the command, address and data received by the slave is controlled by `SPI_RD_BIT_ORDER`.

* **LP-SPI**

    - When operating as a master:
        * The bit order of the command, address and data sent by the LP-SPI master is controlled by `LP_SPI_WR_BIT_ORDER`.
        * The bit order of the data received by the master is controlled by `LP_SPI_RD_BIT_ORDER`.

    - When operating as a slave:
        * The bit order of the data sent by the LP-SPI slave is controlled by `LP_SPI_WR_BIT_ORDER`.
        * The bit order of the command, address and data received by the slave is controlled by `LP_SPI_RD_BIT_ORDER`.

Tables 43.5-6 and 43.5-7 show the functions of `SPI_RD/WR_BIT_ORDER` and `LP_SPI_RD/WR_BIT_ORDER`.
```