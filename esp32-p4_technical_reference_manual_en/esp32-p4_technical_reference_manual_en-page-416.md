

```markdown
DMA2D_OUT_DSCR_TASK_OVF_CHn_INT: Triggered when the number of cached DMA2D_TASK_OUT_DSCR_READY_CHn task exceeds the maximum capacity of the task buffer.
DMA2D_OUTFIFO_RO_OVF_CHO_INT (only channel 0): Triggered when the buffer for macroblock reordering or color space conversion in TX direction overflows.
DMA2D_OUTFIFO_RO_UDFCHO_INT (only channel 0): Triggered when the buffer for macroblock reordering or color space conversion in TX direction underflows.

## 6.7 Programming Procedures

The clock gating for the 2D-DMA can be configured via HP_SYS_CLKRST_DMA2D_SYS_CLK_EN, and is enabled by default. The 2D-DMA can be reset globally by configuring HP_SYS_CLKRST_RST_EN_AHB/AXI_PDMA.

### 6.7.1 General Configurations for 2D-DMA

Configure the accessible address space of internal and external memory and burst length according to Section 6.4.11.

### 6.7.2 Mode-Specific Configurations for 2D-DMA

*   1D Mode: No specific configuration required.
*   2D-MODO Mode: No specific configuration required.
*   2D-MOD1 Mode: For JPEG, configure DMA2D_IN_MACRO_BLOCK_SIZE_CHn or DMA2D_OUT_MACRO_BLOCK_SIZE_CHn to choose a macroblock size out of the three available options (horizontal × vertical): 8 pixels × 8 pixels, 8 pixels × 16 pixels, and 16 pixels × 16 pixels. For more information about macroblock size, see Chapter 35 JPEG Codec. For correspondence between macroblock size, hb, and vb of descriptors, see Table 6.4-4 and Table 6.4-5.
*   DSCR-PORT Mode: Set DMA2D_OUT_DSCR_PORT_EN_CHn to enter this mode. This mode is specifically designed for PPA. For details, see Chapter 37 Pixel-Processing Accelerator (PPA).

### 6.7.3 Configurations for 2D-DMA's Transmit Channel

To transmit data, 2D-DMA's transmit channel should be configured by software as follows:

1.  Set DMA2D_OUT_RST_CHn first to 1 and then to 0, to reset the state machine of 2D-DMA's transmit channel and FIFO pointer.
2.  Load an outlink, and configure DMA2D_OUTLINK_ADDR_CHn with address of the first transmit descriptor.
3.  Configure DMA2D_OUT_PERI_SEL_CHn with the value corresponding to the peripheral to be connected, as shown in Table 6.4-2.
4.  Set DMA2D_OUTLINK_START_CHn to enable 2D-DMA's transmit channel for data transfer.
5.  Configure and enable the corresponding peripheral. See details in individual chapters of these peripherals.
6.  Wait for the DMA2D_OUT_EOF_CHn_INT interrupt, which indicates the completion of data transfer.
```