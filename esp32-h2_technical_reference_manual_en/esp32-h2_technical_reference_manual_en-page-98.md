

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE)

GoBack

## 2.10 Registers

The addresses in this section are relative to RISC-V Trace Encoder base address provided in Table 4.3-2 in Chapter 4 System and Memory.

### Register 2.1. TRACE_MEM_START_ADDR_REG (0x0000)

```
┌───────────────────────────────┬────────┐
│                                │   0    │
├───────────────────────────────┼────────┤
│          31                    │        │
│                               ──┼────────┤
│         0                      │ Reset  │
└───────────────────────────────┴────────┘

TRACE_MEM_START_ADDR Configures the start address of trace memory. (R/W)
```

### Register 2.2. TRACE_MEM_END_ADDR_REG (0x0004)

```
┌───────────────────────────────┬────────┐
│                                │   0    │
├───────────────────────────────┼────────┤
│          31                    │        │
│                               ──┼────────┤
│         0                      │ Reset  │
└───────────────────────────────┴────────┘

TRACE_MEM_END_ADDR Configures the end address of trace memory. (R/W)
```

### Register 2.3. TRACE_MEM_CURRENT_ADDR_REG (0x0008)

```
┌───────────────────────────────┬────────┐
│                                │   0    │
├───────────────────────────────┼────────┤
│          31                    │        │
│                               ──┼────────┤
│         0                      │ Reset  │
└───────────────────────────────┴────────┘

TRACE_MEM_CURRENT_ADDR Represents the current memory address for writing. (RO)
```

Espressif Systems
98
ESP32-H2 TRM (Version 1.1)

Submit Documentation Feedback
```