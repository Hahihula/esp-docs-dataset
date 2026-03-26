

```markdown
Chapter 37 Pixel-Processing Accelerator (PPA)

GoBack

3. Select the input and output channels of 2D-DMA:
    * Write 0x1 to `DMA2D_OUT_PERI_SEL_CHx` to allocate one 2D-DMA output channel to the PPA SRM input
    * Write 0x1 to `DMA2D_IN_PERI_SEL_CHx` to allocate one 2D-DMA input channel to the PPA SRM output

4. Enable descriptor interface for 2D-DMA channels used by PPA:
    * Write 1 to `DMA2D_OUT_DSCR_PORT_EN_CHx` to enable descriptor interface
    * Write 1 to `DMA2D_IN_DSCR_PORT_EN_CHx` to enable descriptor interface

5. Configure the descriptor interface completion parameters of 2D-DMA:
    * Configure the horizontal completion parameters via `DMA2D_OUT_DSCR_PORT_BLK_H_CHx`. See Table 37.5-5 for details
    * Configure the vertical completion parameters via `DMA2D_OUT_DSCR_PORT_BLK_V_CHx`. See Table 37.5-5 for details

6. Enable the input and output channels of 2D-DMA:
    * Write 1 to `DMA2D_OUTLINK_START_CHx` to enable the output channel of 2D-DMA
    * Write 1 to `DMA2D_INLINK_START_CHx` to enable the input channel of 2D-DMA

7. Configure SRM parameters:
    * Configure the size of image blocks to be processed via `PPA_SRM_BK_SIZE_SEL`
    * Configure SRM input data format via `PPA_SRM_RX_CM`
    * Configure SRM output data format via `PPA_SRM_TX_CM`
    * Configure the integer part of the horizontal scaling factor via `PPA_SRM_SCAL_X_INT`
    * Configure the fractional part of the horizontal scaling factor via `PPA_SRM_SCAL_X_FRAG`
    * Configure the integer part of the vertical scaling factor via `PPA_SRM_SCAL_Y_INT`
    * Configure the fractional part of the vertical scaling factor via `PPA_SRM_SCAL_Y_FRAG`
    * Configure the counterclockwise rotation angle via `PPA_SRM_ROTATE_ANGLE`
    * Enable horizontal mirroring via `PPA_SRM_MIRROR_X`
    * Enable vertical mirroring via `PPA_SRM_MIRROR_Y`

8. Write 1 to `PPA_SCAL_ROTATE_START` to start the SRM workflow.

37.7.3 BLEND CLUT Configuration

1. In the FIFO mode:
    * Write 0 to `PPA_APB_FIFO_MASK` to enter the FIFO mode
    * Write data to `PPA_RDWR_WORD_BLEndo_CLUT` to initialize the background layer's CLUT
    * Write data to `PPA_RDWR_WORD_BLEND1_CLUT` to initialize the foreground layer's CLUT

2. In the MEM mode:
    * Write 1 to `PPA_APB_FIFO_MASK` to enter the MEM mode
```