

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE)

GoBack

## 2.10 Registers

The addresses in this section are relative to RISC-V Trace Encoder base address provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 2.1. TRACE_MEM_START_ADDR_REG (0x0000)

```markdown
| 31 | 0 |
|----|---|
|    | 0x000000 |
```

TRACE_MEM_START_ADDR Configures the start address of trace memory. (R/W)

### Register 2.2. TRACE_MEM_END_ADDR_REG (0x0004)

```markdown
| 31 | 0 |
|----|---|
|    | 0xffffffff |
```

TRACE_MEM_END_ADDR Configures the end address of trace memory. (R/W)

### Register 2.3. TRACE_MEM_CURRENT_ADDR_REG (0x0008)

```markdown
| 31 | 0 |
|----|---|
|    | 0x000000 |
```

TRACE_MEM_CURRENT_ADDR Represents the current memory address for writing. (RO)
```