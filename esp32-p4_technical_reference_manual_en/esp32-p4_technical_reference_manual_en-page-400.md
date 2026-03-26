

```markdown
- 2D-MOD1 mode: enabled by setting the 2DEN field of DW0 to 1 and the mod field of DW2 to 1. In this mode, the 2D-DMA reads or writes multiple macroblocks from the starting address of the HA*VA image until the HA*VA image has been fully read or written. For JPEG, it is necessary to configure DMA2D_IN_MACRO_BLOCK_SIZE_CHn or DMA2D_OUT_MACRO_BLOCK_SIZE_CHn to choose a macroblock size out of the three available options (horizontal × vertical): 8 pixels × 8 pixels, 8 pixels × 16 pixels, and 16 pixels × 16 pixels. For more information about macroblock size, see Chapter 35 JPEG Codec. For correspondence between macroblock size, hb, and vb of descriptors, see Table 6.4-4 and Table 6.4-5.

- DSCR-PORT mode: enabled by setting the 2DEN field of DW0 to 1, the mod field of DW2 to 0, and the DMA2D_OUT_DSCR_PORT_EN_CHn bit or the DMA2D_IN_DSCR_PORT_EN_CHn bit to 1. This mode is specifically designed for PPA. For details, see Chapter 37 Pixel-Processing Accelerator (PPA).

1D Mode, 2D-MODO Mode, 2D-MOD1 Mode, and DSCR-PORT support both peripheral-to-memory and memory-to-peripheral data transfers. Only 1D Mode and 2D-MODO Mode support memory-to-memory data transfers.

## 6.4.2 Linked List

Figure 6.4-1 shows the structure of a linked list. An outlink and an inlink have the same structure. A linked list is formed by one or more descriptors, and each descriptor consists of five words. Linked lists should be stored in the memory for the 2D-DMA to be able to use them. The meanings of a descriptor’s fields are shown in Table 6.4-1.

**Note:** DMA2D_OUT is the prefix of transmit channel registers, and DMA2D_IN is the prefix of receive channel registers.
```
Figure 6.4-1. Structure of a Linked List

| DW0 | owner | eof | 2DEN | err_eof | length [13:0] / hb | size[13:0] / vb |
|-----|-------|-----|------|---------|--------------------|-----------------|
|     |       |     |      |         |                    |                 |

| DW1 | pbyte [3:0] | length [27:14] / HA | size [27:14] / VA |
|-----|-------------|---------------------|-------------------|

| DW2 | Reserved [2:0] | mod | X | Y |

| DW3 | Buffer address pointer |

| DW4 | Next descriptor address |
```