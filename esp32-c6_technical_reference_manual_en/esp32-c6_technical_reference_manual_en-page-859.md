

```markdown
Figure 28.8-2. Timing Compensation Example in GP-SPI2 as Master

In Figure 28.8-2, “p1” is the point of input data of Timing Module. “p2” is the point of output data of Timing Module. Since the input data FSPIQ is unaligned to FSPID, the read data of GP-SPI2 will be wrong without the timing compensation.

To get the correct read data, follow the settings below. Assuming f_clk_spi_mst equals to f_SPI_CLK:

- Delay FSPID for two cycles at the falling edge of clk_spi_mst.
- Delay FSPIQ for one cycle at the falling edge of clk_spi_mst.
- Add one extra dummy cycle.

When GP-SPI2 works as slave, if the bit SPI_RSCK_DATA_OUT in register SPI_SLAVE_REG is set to 1, the output data is sent at latch edge, which is half an SPI clock cycle earlier. This can be used for slave mode timing compensation.



## 28.9 Interrupts

### Interrupt Summary

GP-SPI2 provides an SPI interface interrupt SPI_INT. When an SPI transfer ends, an interrupt is generated in GP-SPI2.

- SPI_DMA_INFIFO_FULL_ERR_INT: triggered when the length of GDMA RX FIFO is shorter than that of actual data transferred.
- SPI_DMA_OUTFIFO_EMPTY_ERR_INT: triggered when the length of GDMA TX FIFO is shorter than that of actual data transferred.
- SPI_SLV_EX_QPI_INT: triggered when Ex_QPI is received correctly in GP-SPI2 as slave and the SPI transfer ends.
```