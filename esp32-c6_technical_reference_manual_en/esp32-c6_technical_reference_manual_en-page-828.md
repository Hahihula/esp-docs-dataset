

```markdown
## 28.5.4 Transfer Types

The transfer types supported by GP-SPI2 when working as a master or a slave are shown on Table 28.5-5.

Table 28.5-5. Supported Transfer Types as Master or Slave

| Mode     | CPU-Controlled Single Transfer | DMA-Controlled Single Transfer | DMA-Controlled Configurable Segmented Transfer | DMA-Controlled Slave Segmented Transfer |
|----------|----------------------------------|----------------------------------|-----------------------------------------------|-------------------------------------------|
| Master   | Full-Duplex                      | Y                                | Y                                             | –                                         |
|          | Half-Duplex                      | Y                                | Y                                             | –                                         |
| Slave    | Full-Duplex                      | Y                                | –                                             | Y                                         |
|          | Half-Duplex                      | Y                                | –                                             | Y                                         |

The following sections provide detailed information about the transfer types listed in the table above.

## 28.5.5 CPU-Controlled Data Transfer

GP-SPI2 provides 16 x 32-bit data buffers, i.e., `SPI_W0_REG ~ SPI_W15_REG`, as shown in Figure 28.5-1.  
CPU-controlled transfer indicates the transfer in which the data to send is from GP-SPI2 data buffer and the received data is stored to GP-SPI2 data buffer. In such transfer, every single transaction needs to be triggered by the CPU after its related registers are configured. For such reason, the CPU-controlled transfer is always single transfer (consisting of only one transaction). CPU-controlled transfer supports full-duplex communication and half-duplex communication.

Figure 28.5-1. Data Buffer Used in CPU-Controlled Transfer

### 28.5.5.1 CPU-Controlled Master Transfer

In a CPU-controlled master full-duplex or half-duplex transfer, the RX or TX data is saved to or sent from `SPI_W0_REG ~ SPI_W15_REG`. The bits `SPI_USR_MOSI_HIGHPART` and `SPI_USR_MISO_HIGHPART` control which buffers are used. See the list below.

*   **TX data**
    - When `SPI_USR_MOSI_HIGHPART` is cleared, i.e., high part mode is disabled, TX data is read from `SPI_W0_REG ~ SPI_W15_REG` and the data address is incremented by 1 on each byte transferred. If
```