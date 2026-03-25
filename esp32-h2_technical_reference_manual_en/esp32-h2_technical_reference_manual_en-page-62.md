

```markdown
Register 1.27. MTIME (0x1808)

MTIME[63:32]  
63 | 32  
---|---  
o | Reset  

MTIME[31:0]  
31 | 0  
---|---  
o | Reset  

MTIME Configures the 64-bit CLINT timer counter value. (R/W)

Register 1.28. MTIMECMP (0x1810)

MTIMECMP[63:32]  
63 | 32  
---|---  
o | Reset  

MTIMECMP[31:0]  
31 | 0  
---|---  
o | Reset  

MTIMECMP Configures the 64-bit machine timer compare value. (R/W)

Register 1.29. USIP (0x1C00)

(reserved)  
USIP  
31 | 1 | 0  
---|---|---  
o | o | Reset  

USIP Configures the pending status of the user software interrupt.
O: Not pending
1: Pending
(R/W)
```