

```markdown
Register 4.67. AHB_DMA_IN_DONE_DES_ADDR_CHn_REG(n: 0-2) (0x0410+0x08*n)

31                                 0
+-----------------------------------------------+
| Ox0                                       Reset |
+-----------------------------------------------+

AHB_DMA_IN_DONE_DES_ADDR_CHn Represents the address of the descriptor corresponding to the completed RX transfer. (RO)


Register 4.68. AHB_DMA_OUT_DONE_DES_ADDR_CHn_REG(n: 0-2) (0x0414+0x08*n)

31                                 0
+-----------------------------------------------+
| Ox0                                       Reset |
+-----------------------------------------------+

AHB_DMA_OUT_DONE_DES_ADDR_CHn Represents the address of the descriptor corresponding to the completed TX transfer. (RO)


4.9.2 GDMA-AXI Registers

The addresses in this section are relative to GDMA-AXI base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```