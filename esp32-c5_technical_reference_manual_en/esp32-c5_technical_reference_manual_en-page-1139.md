

```markdown
| SPI_ADDR_REG | The second word, stores the new value to `SPI_ADDR_REG`. |
|--------------|----------------------------------------------------------|
| SPI_CTRL_REG | The third word, stores the new value to `SPI_CTRL_REG`.  |
| SPI_CLOCK_REG| The fourth word, stores the new value to `SPI_CLOCK_REG`. |
| SPI_USER_REG | The fifth word, stores the new value to `SPI_USER_REG`.   |
| SPI_USER1_REG| The sixth word, stores the new value to `SPI_USER1_REG`. |

Table 33.5-12. BM Bit Value and Register to Be Updated in This Example

<table><thead><tr><th>BM Bit</th><th>Value</th><th>Register</th><th>BM Bit</th><th>Value</th><th>Register</th></tr></thead><tbody><tr><td>0</td><td>1</td><td>SPI_ADDR_REG</td><td>7</td><td>0</td><td>SPI_MISC_REG</td></tr><tr><td>1</td><td>1</td><td>SPI_CTRL_REG</td><td>8</td><td>0</td><td>SPI_DIN_MODE_REG</td></tr><tr><td>2</td><td>1</td><td>SPI_CLOCK_REG</td><td>9</td><td>0</td><td>SPI_DIN_NUM_REG</td></tr><tr><td>3</td><td>1</td><td>SPI_USER_REG</td><td>10</td><td>0</td><td>SPI_DOUT_MODE_REG</td></tr><tr><td>4</td><td>1</td><td>SPI_USER1_REG</td><td>11</td><td>0</td><td>SPI_DMA_CONF_REG</td></tr><tr><td>5</td><td>0</td><td>SPI_USER2_REG</td><td>12</td><td>0</td><td>SPI_DMA_INT_ENA_REG</td></tr><tr><td>6</td><td>0</td><td>SPI_MS_DLEN_REG</td><td>13</td><td>0</td><td>SPI_DMA_INT_CLR_REG</td></tr></tbody></table>

Notes

In a DMA-controlled configurable segmented transfer, please pay special attention to the following bits:

* `SPI_USR_CONF`: set `SPI_USR_CONF` before `SPI_USR` is set, to enable this transfer.
* `SPI_USR_CONF_NXT`: if segment *i* is not the final transaction of this whole DMA-controlled transfer, its `SPI_USR_CONF_NXT` bit should be set to 1.
* `SPI_CONF_BITLEN`: GP-SPI2 CS setup time and hold time are programmable independently in each segment, see Section 33.6 for detailed configuration. The CS high time in each segment is about:

    `(SPI_CONF_BITLEN + 5) × T_AHB_CLK`

The CS high time in `CONF` state can be set from 62.5 ns~3.2768 ms when $f_{AHB\_CLK}$ is 80 MHz.
`(SPI_CONF_BITLEN + 5)` will overflow from `(0x40000 - SPI_CONF_BITLEN - 5)` if `SPI_CONF_BITLEN` is larger than 0xFFFF.

## 33.5.10 GP-SPI2 Works as Slave

GP-SPI2 can be used as a slave to communicate with an SPI master. As a slave, GP-SPI2 supports 1-bit SPI, 2-bit dual SPI, 4-bit quad SPI, and QPI modes, with specific communication formats. To enable this mode, set `SPI_SLAVE_MODE` in register `SPI_SLAVE_REG`.

The CS signal must be held low during the transfer, and its falling and rising edges indicate the start and end of a single or segmented transfer.

Take CS low-level effective as an example, when GP-SPI is used as a slave, the CS invalid duration (high-level) between each SPI transfer should not be less than 8 $T_{AHB\_CLK}$ to ensure that each transfer can end normally.
```