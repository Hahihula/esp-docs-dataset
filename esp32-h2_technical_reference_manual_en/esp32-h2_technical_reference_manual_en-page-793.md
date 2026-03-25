

```markdown
| CONF bufferi | Note                                                                                                                                                                                                 |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SPI_BIT_MAP_WORD | The first word in this buffer. Its value is 0xA000001F in this example when the SPI_DMA_SEG_MAGIC_VALUE is set to 0xA. As shown in Table 29.5-12, bits 0, 1, 2, 3, and 4 are set, indicating the following registers will be updated. |
| SPI_ADDR_REG   | The second word, stores the new value to SPI_ADDR_REG.                                                                                                                                                |
| SPI_CTRL_REG   | The third word, stores the new value to SPI_CTRL_REG.                                                                                                                                                  |
| SPI_CLOCK_REG  | The fourth word, stores the new value to SPI_CLOCK_REG.                                                                                                                                             |
| SPI_USER_REG   | The fifth word, stores the new value to SPI_USER_REG.                                                                                                                                                 |
| SPI_USER1_REG  | The sixth word, stores the new value to SPI_USER1_REG.                                                                                                                                             |

Table 29.5-12. BM Bit Value v.s. Register to Be Updated in This Example

<table><thead><tr><td>BM Bit</td><td>Value</td><td>Register Name</td><td>BM Bit</td><td>Value</td><td>Register Name</td></tr></thead><tbody><tr><td>0</td><td>1</td><td>SPI_ADDR_REG</td><td>7</td><td>0</td><td>SPI_MISC_REG</td></tr><tr><td>1</td><td>1</td><td>SPI_CTRL_REG</td><td>8</td><td>0</td><td>SPI_DIN_MODE_REG</td></tr><tr><td>2</td><td>1</td><td>SPI_CLOCK_REG</td><td>9</td><td>0</td><td>SPI_DIN_NUM_REG</td></tr><tr><td>3</td><td>1</td><td>SPI_USER_REG</td><td>10</td><td>0</td><td>SPI_DOUT_MODE_REG</td></tr><tr><td>4</td><td>1</td><td>SPI_USER1_REG</td><td>11</td><td>0</td><td>SPI_DMA_CONF_REG</td></tr><tr><td>5</td><td>0</td><td>SPI_USER2_REG</td><td>12</td><td>0</td><td>SPI_DMA_INT_ENA_REG</td></tr><tr><td>6</td><td>0</td><td>SPI_MS_DLEN_REG</td><td>13</td><td>0</td><td>SPI_DMA_INT_CLR_REG</td></tr></tbody></table>

Notes:

In a DMA-controlled configurable segmented transfer, please pay special attention to the following bits:
* SPI_USR_CONF: set SPI_USR_CONF before SPI_USR is set, to enable this transfer.
* SPI_USR_CONF_NXT: if segmenti is not the final transaction of this whole DMA-controlled transfer, its SPI_USR_CONF_NXT bit should be set to 1.
* SPI_CONF_BITLEN: GP-SPI2 CS setup time and hold time are programmable independently in each segment, see Section 29.6 for detailed configuration. The CS high time in each segment is about:

(SPI_CONF_BITLEN + 5) × T<sub>AHB_CLK</sub>

The CS high time in CONF state can be set from 156.25 ns to 8.1918 ms when f<sub>APB_CLK</sub> is 32 MHz. (SPI_CONF_BITLEN + 5) will overflow from (0x40000 - SPI_CONF_BITLEN - 5) if SPI_CONF_BITLEN is larger than 0x3FFFA.

## 29.5.10 GP-SPI2 Works as a Slave

GP-SPI2 can be used as a slave to communicate with an SPI master. As a slave, GP-SPI2 supports 1-bit SPI, 2-bit dual SPI, 4-bit quad SPI, and QPI modes, with specific communication formats. To enable this mode, set SPI_SLAVE_MODE in register SPI_SLAVE_REG.
```