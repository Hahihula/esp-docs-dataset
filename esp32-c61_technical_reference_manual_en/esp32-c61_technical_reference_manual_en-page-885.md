

```markdown
always single transfer (consisting of only one transaction). CPU-controlled transfer supports full-duplex communication and half-duplex communication.

Figure 26.5-1. Data Buffer Used in CPU-Controlled Transfer

## 26.5.6.1 CPU-Controlled Master Transfer

In a CPU-controlled master full-duplex or half-duplex transfer, the RX or TX data is saved to or sent from `SPI_W0_REG`~`SPI_W15_REG`. The bits `SPI_USR_MOSI_HIGHPART` and `SPI_USR_MISO_HIGHPART` control which buffers are used. See the description below.

*   **TX data**

    -   When `SPI_USR_MOSI_HIGHPART` is cleared, i.e., high part mode is disabled, TX data is read from `SPI_W0_REG`~`SPI_W15_REG` and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 64, the data in `SPI_W0_REG`~`SPI_W15_REG` may be sent more than once.

        Take each 256 bytes as a cycle:

        *   The first 64 bytes (Byte 0~Byte 63) are read from `SPI_W0_REG`~`SPI_W15_REG`, sequentially.
        *   Byte 64~Byte 255 are read from `SPI_W15_REG[31:24]` repeatedly.
        *   Byte 256~Byte 319 (the first 64 bytes in another 256 bytes) are read from `SPI_W0_REG`~`SPI_W15_REG` again, sequentially, same as the behaviors described above.

    For instance: to send 258 bytes (Byte 0~Byte 257), the data is read from the registers as follows:

        *   The first 64 bytes (Byte 0~Byte 63) are read from `SPI_W0_REG`~`SPI_W15_REG`, sequentially.
        *   Byte 64~Byte 255 are read from `SPI_W15_REG[31:24]` repeatedly.
        *   The other bytes (Byte 256 and Byte 257) are read from `SPI_W0_REG[7:0]` and `SPI_W0_REG[15:8]` again, sequentially. The logic is:

            -   The address to read data for Byte 256 is the result of `(256 % 64 = 0)`, i.e., `SPI_W0_REG[7:0]`.
            -   The address to read data for Byte 257 is the result of `(257 % 64 = 1)`, i.e., `SPI_W0_REG[15:8]`.

    -   When `SPI_USR_MOSI_HIGHPART` is set, i.e., high part mode is enabled, TX data is read from `SPI_W8_REG`~`SPI_W15_REG` and the data address is incremented by 1 on each byte transferred. If
```