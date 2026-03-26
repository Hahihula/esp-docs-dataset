

```markdown
| Name         | Description                                      | Address | Access |
|--------------|--------------------------------------------------|---------|--------|
| dcsr          | Debug Control and Status                         | 0x7B0   | R/W    |
| dpc           | Debug PC                                         | 0x7B1   | R/W    |
| dscratch0     | Debug Scratch Register 0                         | 0x7B2   | R/W    |
| dscratch1     | Debug Scratch Register 1                         | 0x7B3   | R/W    |

All debug module registers are implemented in accordance with the specification RISC-V External Debug Support Version 0.13. For more information, refer to the specification.
```

### 3.5.4 Registers

The following is a detailed description of the debug CSR supported by the LP CPU.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```