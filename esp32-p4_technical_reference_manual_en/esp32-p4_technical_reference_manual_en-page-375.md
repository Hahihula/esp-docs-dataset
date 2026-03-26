

```markdown
Register 5.11. DMAC_CHn_CTLO_REG (n: 1-4) (0x0100*n + 0x0018)

Continued from the previous page...

DMAC_CHn_DST_TR_WIDTH Configures destination transfer width.

0x0: 8 bits
0x1: 16 bits
0x2: 32 bits
0x3: 64 bits
(R/W)

DMAC_CHn_SRC_MSIZE Configures the length of the source burst transaction. Every time the handshaking interface requests for a source burst transaction, the read value of this field from the source is the number of data items, each of width DMAC_CHn_SRC_TR_WIDTH.

0x0: 1 data item
0x1: 4 data items
0x2: 8 data items
0x3: 16 data items
0x4: 32 data items
0x5: 64 data items
0x6: 128 data items
0x7: 256 data items
0x8: 512 data items
0x9: 1024 data items
(R/W)

DMAC_CHn_DST_MSIZE Configures the length of the destination burst transaction. Every time the handshaking interface requests for a destination burst transaction, the read value of this field from the destination is the number of data items, each of width DMAC_CHn_SRC_TR_WIDTH.

0x0: 1 data item
0x1: 4 data items
0x2: 8 data items
0x3: 16 data items
0x4: 32 data items
0x5: 64 data items
0x6: 128 data items
0x7: 256 data items
0x8: 512 data items
0x9: 1024 data items
(R/W)

Continued on the next page...
```