

```markdown
## 29.5.4 Unaligned Byte Transfer

* When used as a master, the GP-SPI master can transmit and receive data by bit, with the bit length equal to `SPI_MS_DATA_BITLEN + 1`. The bit length must be a multiple of 1/2/4/8 in 1-line, 2-line, 4-line, and 8-line modes, respectively.
    - When transmitting data that is not a multiple of 8 bits, the software must pad the remaining bits to form a complete byte.
    - When receiving data that is not a multiple of 8 bits, the remaining bits are still received as a full byte.
* When used as a slave, the GP-SPI slave can also transmit and receive data by bit, with the bit length being a multiple of 1/2/4/8 in 1-line, 2-line, 4-line, and 8-line modes, respectively.
    - When transmitting data that is not a multiple of 8 bits, the software must pad the remaining bits to form a complete byte.
    - When receiving data that is not a multiple of 8 bits, the remaining bits are still received as a full byte. The total received length can be obtained via `SPI_SLV_DATA_BITLEN`, and the number of valid bits in the last byte can be identified by using `SPI_SLV_LAST_BYTE_STRB`.

**Note:**
* Regardless of whether GP-SPI is used as a master or a slave, the bit order for transmitting/receiving partial bytes follows the configured setting.

## 29.5.5 Transfer Types

The transfer types supported by GP-SPI2 when working as a master or a slave are shown on Table 29.5-5.

Table 29.5-5. Supported Transfer Types as Master or Slave

| Mode     | CPU-Controlled Single Transfer | DMA-Controlled Single Transfer | DMA-Controlled Configurable Segmented Transfer | DMA-Controlled Slave Segmented Transfer |
|----------|----------------------------------|----------------------------------|-----------------------------------------------|-------------------------------------------|
| **Master** | Full-Duplex                      | Y                                | Y                                             | –                                         |
|          | Half-Duplex                      | Y                                | Y                                             | –                                         |
| **Slave**  | Full-Duplex                      | Y                                | –                                             | Y                                         |
|          | Half-Duplex                      | Y                                | –                                             | Y                                         |

The following sections provide detailed information about the transfer types listed in the table above.

## 29.5.6 CPU-Controlled Data Transfer

GP-SPI2 provides 16 x 32-bit data buffers, i.e., `SPI_W0_REG ~ SPI_W15_REG`, as shown in Figure 29.5-1. CPU-controlled transfer indicates the transfer in which the data to send is from GP-SPI2 data buffer and the received data is stored to GP-SPI2 data buffer. In such a transfer, every single transaction needs to be triggered by the CPU after its related registers are configured. For such reason, the CPU-controlled transfer is
```