

```markdown
Register 6.17. DMA2D_IN_CONFO_CHn_REG (n: 0-2) (0x0500+0x100*n)
```

Continued from the previous page...

```markdown
DMA2D_IN_MACRO_BLOCK_SIZE_CHn Configures macroblock size for RX channel n. Used only in 2D-MOD1 mode.
```
```markdown
0: 8 * 8 pixels

1: 8 * 16 pixels

2: 16 * 16 pixels

3: No macroblock
```

(R/W)

```markdown
DMA2D_IN_DSCR_PORT_EN_CHn Configures whether to enable the DSCR-PORT mode for RX channel n.
```
```markdown
0: Disable

1: Enable
```

(R/W)

```markdown
DMA2D_IN_REORDER_EN_CHO Configures whether to enable macroblock reordering for RX channel 0.
```
```markdown
0: Disable

1: Enable
```

(R/W)

```markdown
DMA2D_IN_RST_CHn Configures whether to reset RX channel n.
```
```markdown
0: Invalid

1: Reset
```

(R/W)

```markdown
DMA2D_IN_CMD_DISABLE_CHn Configures reset command for RX channel n.
```
```markdown
0: Set 0 after reset release

1: Pause transfers before reset
```

(R/W)

```markdown
DMA2D_IN_ARB_WEIGHT_OPT_DIS_CHn Configures whether to enable weight optimization for RX channel n.
```
```markdown
0: Enable

1: Disable
```

(R/W)
```