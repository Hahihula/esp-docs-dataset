

```markdown
## 43.5.4 Unaligned Byte Transfer

* When operating as a master, GP-SPI sends and receives data in bits. The bit length is equal to `SPI_MS_DATA_BITLEN + 1`, a multiple of 1/2/4/8 in 1/2/4/8-bit mode.
    - When sending data whose length is not an integer multiple of 8 bits, the software needs to fill the last part of the data less than 8 bits into a full 1-byte data.
    - When receiving data whose length is not an integer multiple of 8 bits, the part less than 1 byte is still received as 1 byte.

* When operating as slave, GP-SPI sends and receives data in bits. The bit length is a multiple of 1/2/4/8 in 1/2/4/8-bit mode.
    - When sending data whose length is not an integer multiple of 8 bits, the software needs to fill the last part of the data less than 8 bits into a full 1-byte data.
    - When receiving data whose length is not an integer multiple of 8 bits, the part less than 1 byte is still received as 1 byte. The total bit length received can be read from `SPI_SLV_DATA_BITLEN`. The valid bits in the last 1 byte is indicated by `SPI_SLV_LAST_BYTE_STRB`.

**Note:**
* No matter working as master or slave, GP-SPI sends and receives the data parts less than 1 byte following the same bit order as the other data bits as configured.
* LP-SPI does not support this unaligned byte transfer.

## 43.5.5 Transfer Types

The transfer types supported by GP-SPI working as a master or a slave are shown in Table 43.5-8.

Table 43.5-8. Supported Transfer Types as Master or Slave

| Mode | CPU-Controlled Single Transfer¹ | DMA-Controlled Single Transfer | DMA-Controlled Configurable Segmented Transfer² | DMA-Controlled Slave Segmented Transfer |
|:------|:----------------------------------|:-------------------------------|:------------------------------------------------|:------------------------------------------|
| **Master** | Full-Duplex                       | Y                              | Y                                              | —                                        |
|          | Half-Duplex                       | Y                              | Y                                              | —                                        |
| **Slave**  | Full-Duplex                       | Y                              | —                                              | Y                                        |
|          | Half-Duplex                       | Y                              | —                                              | Y                                        |

¹ LP-SPI supports only the CPU-controlled single transfer.
² GP-SPI3 does not support DMA-controlled configurable segmented transfer.

The following sections provide detailed information about the transfer types listed in the table above.

## 43.5.6 CPU-Controlled Data Transfer
```