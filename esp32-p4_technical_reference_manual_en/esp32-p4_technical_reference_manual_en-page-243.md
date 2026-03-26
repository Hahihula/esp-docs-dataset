

```markdown
Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI)

GoBack

## 4.7 Programming Procedures

The clock gating for GDMA can be configured via HP_SYS_CLKRST_AHB/AXI_PDMA_SYS_CLK_EN, and is enabled by default. GDMA can be reset by configuring HP_SYS_CLKRST_RST_EN_AHB/AXI_PDMA.

### 4.7.1 Programming Procedures for GDMA's Transmit Channel

To transmit data, GDMA's transmit channel should be configured by software as follows:

1. Set AHB/AXI_DMA_OUT_RST_ChN first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer.

2. Load an outlink, and configure AHB/AXI_DMA_OUTLINK_ADDR_ChN with address of the first transmit descriptor.

3. Configure AHB/AXI_DMA_PERI_OUT_SEL_ChN with the value corresponding to the peripheral to be connected, as shown in Table 4.4-1 and Table 4.4-2.

4. Set AHB/AXI_DMA_OUTLINK_START_ChN to enable GDMA's transmit channel for data transfer.

5. Configure and enable the corresponding peripheral (SPI2, UHCI (UART0 or UART1), I2S, AES, SHA, and ADC). See details in individual chapters of these peripherals.

6. Wait for the AHB/AXI_DMA_OUT_TOTAL_EOF_ChN_INT interrupt, which indicates the completion of data transfer.

### 4.7.2 Programming Procedures for GDMA's Receive Channel

To receive data, GDMA's receive channel should be configured by software as follows:

1. Set AHB/AXI_DMA_IN_RST_ChN first to 1 and then to 0, to reset the state machine of GDMA's receive channel and FIFO pointer.

2. Load an inlink, and configure AHB/AXI_DMA_INLINK_ADDR_ChN with address of the first receive descriptor.

3. Configure AHB/AXI_DMA_PERI_IN_SEL_ChN with the value corresponding to the peripheral to be connected, as shown in Table 4.4-1 and Table 4.4-2.

4. Set AHB/AXI_DMA_INLINK_START_ChN to enable GDMA's receive channel for data transfer.

5. Configure and enable the corresponding peripheral (SPI2, UHCI (UART0 or UART1), I2S, AES, SHA, and ADC). See details in individual chapters of these peripherals.

### 4.7.3 Programming Procedures for Memory-to-Memory Transfer

To transfer data from one memory location to another, GDMA should be configured by software as follows:

1. Set AHB/AXI_DMA_OUT_RST_ChN first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer.

2. Set AHB/AXI_DMA_IN_RST_ChN first to 1 and then to 0, to reset the state machine of GDMA's receive channel and FIFO pointer.
```