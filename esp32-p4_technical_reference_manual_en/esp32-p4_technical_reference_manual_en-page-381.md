

```markdown
Register 5.15. DMAC_CHn_LLPO_REG (n: 1-4) (0x0100*n + 0x0128)

DMAC_CHn_LMS Selects the AXI master for accessing LLI.
O: AXI Master 1
1: AXI Master 2
(R/W)

DMAC_CHn_LOCO Configures the starting address of the first linked list item in memory. The six least significant bits (LSB) of the starting address are not stored because it is assumed that the address is 64-byte aligned. (R/W)
```

```markdown
Register 5.16. DMAC_CHn_BLK_TFR_RESUMEREQO_REG (n: 1-4) (0x0100*n + 0x0148)

DMAC_CHn_BLK_TFR_RESUMEREQ Configures whether to request to resume block transfer during linked-list or shadow-register-based multi-block transfer.
O: Do not request to resume block transfer
1: Request to resume block transfer
(WO)
```