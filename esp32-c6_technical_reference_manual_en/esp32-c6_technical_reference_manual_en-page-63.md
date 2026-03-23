

```markdown
Chapter 1 High-Performance CPU

Register 1.27. MTIME (0x1808)

MTIME[63:32]  
MTIME[31:0]

MTIME Configures the 64-bit CLINT timer counter value. (R/W)


Register 1.28. MTIMECMP (0x1810)

MTIMECMP[63:32]  
MTIMECMP[31:0]

MTIMECMP Configures the 64-bit machine timer compare value. (R/W)


Register 1.29. USIP (0x1C00)

(reserved)  
USIP

USIP Configures the pending status of the user software interrupt.
0: Not pending
1: Pending
(R/W)
```