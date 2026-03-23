

```markdown
| State | Control Registers for 1-bit Mode FSPI Bus | Control Registers for 2-bit Mode FSPI Bus | Control Registers for 4-bit Mode FSPI Bus |
|-------|--------------------------------------------|-------------------------------------------|---------------------------------------------|
| DOUT  | SPI_USR_MOSI<br>SPI_MS_DATA_BITLEN        | SPI_USR_MOSI<br>SPI_MS_DATA_BITLEN<br>SPI_FWRITE_DUAL | SPI_USR_MOSI<br>SPI_MS_DATA_BITLEN<br>SPI_FWRITE_QUAD |
```

As shown in Table 27.5-7, the registers in each cell should be configured to set the FSPI bus to corresponding bit mode, i.e. the mode shown in the table header, at a specific state (corresponding to the first column).

## Configuration

For instance, when GP-SPI2 reads data, and
* CMD is in 1-bit mode
* ADDR is in 2-bit mode
* DUMMY is 8 clock cycles
* DIN is in 4-bit mode

The register configuration can be as follows:

1. Configure CMD state related registers.
    * Configure the required command value in `SPI_USR_COMMAND_VALUE`.
    * Configure command bit length in `SPI_USR_COMMAND_BITLEN`. `SPI_USR_COMMAND_BITLEN` = expected bit length - 1.
    * Set `SPI_USR_COMMAND`.
    * Clear `SPI_FCMD_DUAL` and `SPI_FCMD_QUAD`.

2. Configure ADDR state related registers.
    * Configure the required address value in `SPI_USR_ADDR_VALUE`.
    * Configure address bit length in `SPI_USR_ADDR_BITLEN`. `SPI_USR_ADDR_BITLEN` = expected bit length - 1.
    * Set `SPI_USR_ADDR` and `SPI_FADDR_DUAL`.
    * Clear `SPI_FADDR_QUAD`.

3. Configure DUMMY state related registers.
    * Configure DUMMY cycles in `SPI_USR_DUMMY_CYCLELEN`. `SPI_USR_DUMMY_CYCLELEN` = expected clock cycles - 1.
    * Set `SPI_USR_DUMMY`.

4. Configure DIN state related registers.
    * Configure read data bit length in `SPI_MS_DATA_BITLEN`. `SPI_MS_DATA_BITLEN` = bit length expected - 1.
```