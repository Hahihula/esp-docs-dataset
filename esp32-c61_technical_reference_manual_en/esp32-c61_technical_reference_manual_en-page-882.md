

```markdown
Chapter 26 SPI Controller (SPI)

GoBack

26.5.3 Bit Read/Write Order Control

* When operating as a master:
    - The bit order of the command, address, and data sent by the GP-SPI master is controlled by `SPI_WR_BIT_ORDER`.
    - The bit order of the data received by the master is controlled by `SPI_RD_BIT_ORDER`.

* When operating as a slave:
    - The bit order of the data sent by the GP-SPI slave is controlled by `SPI_WR_BIT_ORDER`.
    - The bit order of the command, address, and data received by the slave is controlled by `SPI_RD_BIT_ORDER`.

Table 26.5-4 shows the functions of `SPI_RD/WR_BIT_ORDER`.
```