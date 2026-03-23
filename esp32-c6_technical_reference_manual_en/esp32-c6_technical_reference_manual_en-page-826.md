

```markdown
Chapter 28 SPI Controller (SPI)

GoBack

28.5.3 Bit Read/Write Order Control

When operating as master:

- The bit order of the command, address, and data sent by the GP-SPI2 master is controlled by `SPI_WR_BIT_ORDER`.
- The bit order of the data received by the master is controlled by `SPI_RD_BIT_ORDER`.

When operating as slave:

- The bit order of the data sent by the GP-SPI2 slave is controlled by `SPI_WR_BIT_ORDER`.
- The bit order of the command, address, and data received by the slave is controlled by `SPI_RD_BIT_ORDER`.

Table 28.5-4 shows the function of SPI_RD/WR_BIT_ORDER.
```