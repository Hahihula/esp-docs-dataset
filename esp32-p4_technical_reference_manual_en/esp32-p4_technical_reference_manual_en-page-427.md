

```markdown
Register 6.1. DMA2D_OUT_CONF0_CHn_REG (n: 0-3) (0x0000+0x100*n)

Continued from the previous page...

DMA2D_OUT_CHECK_OWNER_CHn Configures whether to enable the owner bit check for TX channel n.
O: Disable
1: Enable
(R/W)

DMA2D_OUT_MEM_BURST_LENGTH_CHn Configures the burst length for TX channel n.
0: 8 bytes
1: 16 bytes
2: 32 bytes
3: 64 bytes
4: 128 bytes
Others: Invalid
(R/W)

DMA2D_OUT_MACRO_BLOCK_SIZE_CHn Configures macroblock size for TX channel n. Used only in 2D-MOD1 mode.
0: 8 * 8 pixels
1: 8 * 16 pixels
2: 16 *16 pixels
3: No macroblock
(R/W)

DMA2D_OUT_DSCR_PORT_EN_CHn Configures whether to enable the DSCR-PORT mode for TX channel n.
O: Disable
1: Enable
(R/W)

DMA2D_OUT_REORDER_EN_CHO Configures whether to enable macroblock reordering for TX channel 0.
O: Disable
1: Enable
(R/W)

DMA2D_OUT_RST_CHn Configures whether to reset TX channel n.
O: Reset release
1: Reset
(R/W)

Continued on the next page...
```