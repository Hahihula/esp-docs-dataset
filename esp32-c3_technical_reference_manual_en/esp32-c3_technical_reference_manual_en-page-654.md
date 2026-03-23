

```markdown
Chapter 27 SPI Controller (SPI)

Register 27.7. SPI_MS_DLEN_REG (0x001C)
```

![Register bit field diagram](image_description_not_provided)

```markdown
SPI_MS_DATA_BITLEN The value of this field is the configured SPI transmission data bit length in master mode DMA-controlled transfer or CPU-controlled transfer. The value is also the configured bit length in slave mode DMA RX controlled transfer. The register value shall be (bit_num - 1). Can be configured in CONF state. (R/W)
```