

```markdown
Note:
Both GP-SPI and LP-SPI provide 16 x 32-bit data buffers:

*   GP-SPI: SPI_W0_REG~SPI_W15_REG
*   LP-SPI: LP_SPI_W0_REG~LP_SPI_W15_REG

The following section illustrates the buffer's structure using GP-SPI data buffer as an example.

Figure 43.5-1 shows the buffer's structure. CPU-controlled transfer indicates the transfer, in which the data to send is from GP-SPI data buffer and the received data is stored to GP-SPI data buffer. In such transfer, every single transaction needs to be triggered by the CPU, after its related registers are configured. For such reason, the CPU-controlled transfer is always single transfer (consisting of only one transaction). CPU-controlled transfer supports full-duplex communication and half-duplex communication.

Figure 43.5-1. Data Buffer Used in CPU-Controlled Transfer

43.5.6.1    CPU-Controlled Master Transfer

In a CPU-controlled master full-duplex or half-duplex transfer, the RX or TX data is saved to or sent from SPI_W0_REG~SPI_W15_REG. The bits SPI_USR_MOSI_HIGHPART and SPI_USR_MISO_HIGHPART control which buffers are used. See the description below.

•   TX data

    – When SPI_USR_MOSI_HIGHPART is cleared, i.e., high part mode is disabled, TX data is read from SPI_W0_REG~SPI_W15_REG and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 64, the data in SPI_W0_REG~SPI_W15_REG may be sent more than once.

    Take each 256 bytes as a cycle:

        *   The first 64 bytes (Byte 0~Byte 63) are read from SPI_W0_REG~SPI_W15_REG, sequentially.
        *   Byte 64~Byte 255 are read from SPI_W15_REG[31:24] repeatedly.
        *   Byte 256~Byte 319 (the first 64 bytes in another 256 bytes) are read from SPI_W0_REG~SPI_W15_REG again, sequentially, same as the behaviors described above.

    For instance: to send 258 bytes (Byte 0~Byte 257), the data is read from the registers as follows:

        *   The first 64 bytes (Byte 0~Byte 63) are read from SPI_W0_REG~SPI_W15_REG, sequentially.
        *   Byte 64~Byte 255 are read from SPI_W15_REG[31:24] repeatedly.
```