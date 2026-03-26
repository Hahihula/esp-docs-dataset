

```markdown
* The other bytes (Byte 256 and Byte 257) are saved to SPI_W0_REG[7:0] and SPI_W0_REG[15:8] again, sequentially. The logic is:
    * The address to save Byte 256 is the result of (256 % 64 = 0), i.e., SPI_W0_REG[7:0].
    * The address to save Byte 257 is the result of (257 % 64 = 1), i.e., SPI_W0_REG[15:8].

- When SPI_USR_MISO_HIGHPART is set, i.e., high part mode is enabled, the RX data is saved to SPI_W8_REG~SPI_W15_REG, and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 32, the content of SPI_W8_REG~SPI_W15_REG may be overwritten.

Take each 256 bytes as a cycle:
* Byte 0~Byte 31 are saved to SPI_W8_REG~SPI_W15_REG, sequentially.
* Byte 32~Byte 255 are saved to SPI_W15_REG[31:24] repeatedly.
* Byte 256~Byte 287 (the first 32 bytes in the another 256 bytes) are saved to SPI_W8_REG~SPI_W15_REG again, sequentially.

For instance: to receive 258 bytes (Byte 0~Byte 257), the data is saved to the registers as follows:
* The first 32 bytes (Byte 0~Byte 31) are saved to SPI_W8_REG~SPI_W15_REG, sequentially.
* Byte 32~Byte 255 are saved to SPI_W15_REG[31:24] repeatedly.
* The other bytes (Byte 256 and Byte 257) are saved to SPI_W8_REG[7:0] and SPI_W8_REG[15:8] again, sequentially. The logic is:
    * The address to save Byte 256 is the result of (256 % 32 = 0), i.e., SPI_W8_REG[7:0].
    * The address to save Byte 257 is the result of (257 % 32 = 1), i.e., SPI_W8_REG[15:8].

Note:
* TX/RX data address mentioned above both are byte-addressable.
    - If high part mode is disabled, Address 0 stands for SPI_W0_REG[7:0], and Address 1 for SPI_W0_REG[15:8], and so on.
    - If high part mode is enabled, Address 0 stands for SPI_W8_REG[7:0], and Address 1 for SPI_W8_REG[15:8], and so on.
        The largest address points to SPI_W15_REG[31:24].
* To avoid any possible error in TX/RX data, such as TX data being sent more than once or RX data being overwritten, please make sure the registers are configured correctly.
* LP-SPI functions similarly, but uses LP-SPI registers and LP-SPI data buffers, as shown in Section 43.12.3.

43.5.6.2 CPU-Controlled Slave Transfer

In a CPU-controlled slave full-duplex or half-duplex transfer, the RX or TX data is saved to or sent from SPI_W0_REG~SPI_W15_REG, which are byte-addressable.
* In full-duplex communication, the address of SPI_W0_REG~SPI_W15_REG starts from 0 and is incremented by 1 on each byte transferred. If the data address is larger than 63, the data in SPI_W0_REG~SPI_W15_REG will be overwritten, same as the behaviors described in the master transfer when high part mode is disabled.
```