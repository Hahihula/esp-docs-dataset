

```markdown
- Set the property of SPI2CLK according to Section 43.7.
- Prepare data according to the selected transfer type:
    - In CPU-controlled MOSI transfer, prepare data in registers `SPI_W0_REG`~`SPI_W15_REG`.
    - In DMA-controlled transfer,
        * configure `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA`,
        * configure DMA TX/RX link,
        * and start DMA TX/RX engine, as described in Section 43.5.7 and Section 43.5.8.
- Configure interrupts and wait for SPI slave to get ready for transfer.
- Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.
- Set `SPI_USR` in register `SPI_CMD_REG` to start the transfer and wait for the configured interrupts.

### 43.5.9.4 Half-Duplex Communication (1/2/4/(8)-bit Mode)

#### Introduction

In this mode, GP-SPI provides CLK and CS signals. Only one side (SPI master or slave) can send data at a time, while the other side receives the data. To enable this communication mode, clear the bit `SPI_DOUTDIN` in register `SPI_USER_REG`. The standard format of SPI half-duplex communication is CMD + [ADDR +] [DUMMY+] [DOUT or DIN]. The states ADDR, DUMMY, DOUT, and DIN are optional, and can be disabled or enabled independently.

As described in Section 43.5.9.2, the properties of GP-SPI states: CMD, ADDR, DUMMY, DOUT and DIN, such as cycle length, value, and parallel bus bit mode, can be set independently. For the register configuration, see Table 43.5-10.

The detailed properties of half-duplex GP-SPI are as follows:

1. **CMD**: 0~16 bits, master output, slave input.
2. **ADDR**: 0~32 bits, master output, slave input.
3. **DUMMY**: 0~256 SPI2CLK/SPI3_CLK cycles, master output, slave input.
4. **DOUT**:
    - 0~512 bits (64 bytes) in CPU-controlled transfer,
    - 0~256 Kbits (32 KB) in DMA-controlled single transfer,
    - and unlimited length in DMA-controlled configurable segmented transfer, master output, slave input.
5. **DIN**:
    - 0~512 bits (64 bytes) in CPU-controlled transfer,
    - 0~256 Kbits (32 KB) in DMA-controlled single transfer,
    - and unlimited length in DMA-controlled configurable segmented transfer, slave output, master input.

GP-SPI2 also supports Double Transfer Rate (DTR) in 1/2/4/8-bit modes, in which data is sent and received at the rising and the falling edges of SPI clock:

- If `SPI_CMD_DTR_EN` is set, the CMD value will be sent in DTR mode; otherwise CMD phase will be in Single Transfer Rate (STR) mode.
- If `SPI_ADDR_DTR_EN` is set, the ADDR value will be sent in DTR mode; otherwise ADDR phase will be in STR mode.
```