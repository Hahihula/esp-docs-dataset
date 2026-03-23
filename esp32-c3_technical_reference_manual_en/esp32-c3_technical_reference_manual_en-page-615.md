

```markdown
single transfers (consisting of only one transaction). CPU-controlled mode supports full-duplex communication and half-duplex communication.

Figure 27.5-1. Data Buffer Used in CPU-Controlled Transfer

## 27.5.5.1 CPU-Controlled Master Mode

In a CPU-controlled master full-duplex or half-duplex transfer, the RX or TX data is saved to or sent from `SPI_W0_REG ~ SPI_W15_REG`. The bits `SPI_USR_MOSI_HIGHPART` and `SPI_USR_MISO_HIGHPART` control which buffers are used, see the list below.

### TX data

- When `SPI_USR_MOSI_HIGHPART` is cleared, i.e., high part mode is disabled, TX data is from `SPI_W0_REG ~ SPI_W15_REG` and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 64, the data in `SPI_W0_REG[7:0] ~ SPI_W15_REG[31:24]` may be sent more than once. For instance, if 66 bytes (byte0 ~ byte65) need to be sent, then the address of byte65 is the result of `(65 % 64 = 1)`, i.e., byte65 is from `SPI_W0_REG[15:8]`, and byte64 is from `SPI_W0_REG[7:0]`. In this case, the content of `SPI_W0_REG[15:0]` may be sent more than once.

- When `SPI_USR_MOSI_HIGHPART` is set, i.e., high part mode is enabled, TX data is from `SPI_W8_REG ~ SPI_W15_REG` and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 32, the data in `SPI_W8_REG[7:0] ~ SPI_W15_REG[31:24]` may be sent more than once.

### RX data

- When `SPI_USR_MISO_HIGHPART` is cleared, i.e., high part mode is disabled, RX data is saved to `SPI_W0_REG ~ SPI_W15_REG`, and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 64, the data in `SPI_W0_REG[7:0] ~ SPI_W15_REG[31:24]` may be overwritten. For instance, when 66 bytes (byte0 ~ byte65) are received, byte65 and byte64 are stored to the addresses of `(65 % 64 = 1)` and `(64 % 64 = 0)`, i.e., `SPI_W0_REG[15:8]` and `SPI_W0_REG[7:0]`. In this case, the content of `SPI_W0_REG[15:0]` may be overwritten.

- When `SPI_USR_MISO_HIGHPART` is set, i.e., high part mode is enabled, the RX data is saved to `SPI_W8_REG ~ SPI_W15_REG`, and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 32, the content of `SPI_W8_REG ~ SPI_W15_REG` may be overwritten.
```