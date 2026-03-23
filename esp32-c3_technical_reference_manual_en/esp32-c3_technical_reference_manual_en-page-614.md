

```markdown
## 27.5.3 Bit Read/Write Order Control

In master mode:

- The bit order of the command, address and data sent by the GP-SPI2 master is controlled by `SPI_WR_BIT_ORDER`.
- The bit order of the data received by the master is controlled by `SPI_RD_BIT_ORDER`.

In slave mode:

- The bit order of the data sent by the GP-SPI2 slave is controlled by `SPI_WR_BIT_ORDER`.
- The bit order of the command, address and data received by the slave is controlled by `SPI_RD_BIT_ORDER`.

Table 27.5-5 shows the function of `SPI_RD/WR_BIT_ORDER`.

### Table 27.5-5. Bit Order Control in GP-SPI2 Master and Slave Modes

| Bit Mode | FSPI Bus Data         | SPI_RD/WR_BIT_ORDER = 0 (MSB)       | SPI_RD/WR_BIT_ORDER = 1 (LSB)      |
|----------|-----------------------|-------------------------------------|------------------------------------|
| 1-bit mode | FSPID or FSPIQ        | B7→B6→B5→B4→B3→B2→B1→B0            | BO→B1→B2→B3→B4→B5→B6→B7           |
| 2-bit mode | FSPIQ                 | B7→B5→B3→B1                        | B1→B3→B5→B7                        |
|          | FSPID                 | B6→B4→B2→B0                        | BO→B2→B4→B6                        |
| 4-bit mode | FSPIHD                | B7→B3                            | B3→B7                              |
|          | FSPIWP                | B6→B2                              | B2→B6                              |
|          | FSPIQ                 | B5→B1                               | B1→B5                              |
|          | FSPID                 | B4→BO                               | BO→B4                              |

## 27.5.4 Transfer Modes

GP-SPI2 supports the following transfers when working as a master or a slave.

### Table 27.5-6. Supported Transfers in Master and Slave Modes

| Mode   | CPU-Controlled Single Transfer | DMA-Controlled Single Transfer | DMA-Controlled Configurable Segmented Transfer | DMA-Controlled Slave Segmented Transfer |
|--------|-------------------------------|--------------------------------|-----------------------------------------------|------------------------------------------|
| Master | Full-Duplex                   | Y                              | Y                                             | –                                        |
|        | Half-Duplex                   | Y                              | Y                                             | –                                        |
| Slave  | Full-Duplex                   | Y                              | –                                             | Y                                        |
|        | Half-Duplex                   | Y                              | –                                             | Y                                        |

The following sections provide detailed information about the transfer modes listed in the table above.

## 27.5.5 CPU-Controlled Data Transfer

GP-SPI2 provides 16 x 32-bit data buffers, i.e., `SPI_WO_REG ~ SPI_W15_REG`, see Figure 27.5-1.
CPU-controlled transfer indicates the transfer, in which the data to send is from GP-SPI2 data buffer and the received data is stored to GP-SPI2 data buffer. In such transfer, every single transaction needs to be triggered by the CPU, after its related registers are configured. For such reason, the CPU-controlled transfer is always
```