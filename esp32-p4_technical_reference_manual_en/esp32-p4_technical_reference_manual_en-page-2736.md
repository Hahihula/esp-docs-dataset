

```markdown
Figure 54.7-1. Linked List Structure


## 54.8 DMA Descriptor Format

Each descriptor consists of four words as shown in 54.8-1. Table 54.8-1, Table 54.8-2, Table 54.8-3, Table 54.8-4 provide the descriptions of these four words.

Figure 54.8-1. Descriptor Format

The DESO field contains control and status information.

Table 54.8-1. DESO Descriptor Field
| Bits | Name    | Description |
|------|---------|-------------|
| 31   | OWNER   | When set to 1, this bit indicates that the descriptor is owned by the DMA Controller. When reset to 0, it indicates that the descriptor is owned by the host. The DMA clears this bit when it completes the data transfer. |
```