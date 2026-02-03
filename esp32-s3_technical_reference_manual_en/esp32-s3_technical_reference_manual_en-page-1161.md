**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header:**
Register 30.9. SPI_MISC_REG (For SPI3 Only) (0x0020)

**Table Description:**
- The table shows the bit layout for Register 30.9, labeled as "SPI_MISC_REG". It includes various bits with their corresponding descriptions and values.

**Bit Descriptions in Markdown Format:**

1. **SPI_CS0_DIS**: SPI CS0 pin enable bit.
   - Value (bit): `1`
   - Description: disable CS0
   - Additional Info: 0: SPI_CS0 signal is from/to CS0 pin, can be configured in CONF state.

2. **SPI_CS1_DIS**: SPI CS1 pin enable bit.
   - Value (bit): `1`
   - Description: disable CS1
   - Additional Info: 0: SPI_CS1 signal is from/to CS1 pin; can be configured in CONF state

3. **SPI_CS2_DIS**: SPI CS2 pin enable bit.
   - Value (bit): `1`
   - Description: disable CS2
   - Additional Info: 0: SPI_CS2 signal is from/to CS2 pin, can be configured in CONF state.

4. **SPI_CK_DIS**: Disable SPI_CLK output; Enable SPI_CLK output configuration options for CONF state.
   - Value (bit): `1`
   - Description: disable or enable SPI_CLK
   - Additional Info: Can be configured in CONF state

5. **SPI_MASTER_CS_POL**: Configure the polarity of SPI CSi line to master mode, active high/low configurations available; can also configure in CONF state.
   - Value (bit): `1`
   - Description: set as low or high
   - Additional Info: Can be configured in CONF state

6. **SPI_SLAVE_CS_POL**: Configure SPI slave input CS polarity with inversion options for CONF state configuration.
   - Value (bit): `1`
   - Description: invert, not change configurations available; can only configure in CONF state.

7. **SPI_CLK_IDLE_EDGE**: Set GP-SPI3 idle edge to high or low when SPI_CLK line is active/inactive respectively
   - Value (bit): `1`
   - Description: set as high or low

8. **SPI_CS_KEEP_ACTIVE**: Keep CS line configuration for bit swap in CONF state.
   - Value (bit): `1`
   - Description: keep lines inactive during bit swap configurations.

9. **SPI_QUAD_DIN_PIN_SWAP**: Quad input pin swap enable; disable quad input swaps
   - Value (bit): `1`
   - Description: set as enabled or disabled

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 1161
- Link Texts:
  - "Submit Documentation Feedback"