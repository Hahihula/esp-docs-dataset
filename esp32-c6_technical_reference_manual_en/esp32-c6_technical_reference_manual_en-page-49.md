

```markdown
Chapter 1 High-Performance CPU  GoBack

Register 1.13. mtval (0x343)

MTVAL Configures machine trap value. This is automatically updated with an exception dependent data which may be useful for handling that exception.  
Data is to be interpreted depending upon exception IDs:  
0x1: Faulting virtual address of instruction  
0x2: Faulting instruction opcode  
0x5: Faulting data address of load operation  
0x7: Faulting data address of store operation  
Note: The value of this register is not valid for other exception IDs and interrupts.  
(R/W)

| 31 | ... | 0 |  
|----|------|---|  
|    |      |   |  
| 0x00000000 | Reset |
```