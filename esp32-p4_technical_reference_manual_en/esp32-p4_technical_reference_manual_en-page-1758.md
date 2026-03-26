

```markdown
In the FIFO mode, access to CLUT is achieved by reading/writing `PPA_RDWWR_WORD_BLENDx_CLUT`, where 0 corresponds to the background channel CLUT and 1 corresponds to the foreground channel CLUT.

Each time this register is read/written, the corresponding read/write address is automatically incremented by 1. The read/write address can be reset by writing 1 and then 0 to `PPA_BLENDx_CLUT_MEM_RST`. The read address can be reset by writing 1 then 0 to `PPA_BLENDx_CLUT_MEM_RDADDR_RST`.

* Write 1 to `PPA_APB_FIFO_MASK` to enter the MEM mode.

In the MEM mode, CLUT can be directly accessed through addresses. The CLUT addresses in the PPA's bus address range are as shown in Table 37.5-3.
```

```markdown
Table 37.5-3. BLEND CLUT Address

| addr[11:10] | addr[9:2]           | addr[1:0] |
|-------------|----------------------|-----------|
| 01: Select BLENDO CLUT | CLUT actual address, 0 ~ 255 | 00        |
| 10: Select BLEND1 CLUT |                      |           |
```

```markdown
37.5.2 PPA 2D-DMA Linked List Configuration

PPA exchanges data with the system memory via 2D-DMA. For both SRM and BLEND, it is necessary to configure the 2D-DMA linked list information for the required image block operations in one go. The 2D-DMA linked list is shown in Figure 37.5-3. For detailed information, please refer to 6 2D-DMA Controller (2D-DMA).
```

```markdown
Figure 37.5-3. 2D-DMA Linked List

The corresponding linked list parameters of PPA are shown in Table 37.5-4.
```
```