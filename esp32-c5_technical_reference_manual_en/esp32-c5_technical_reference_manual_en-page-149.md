

# Chapter 3 RISC-V Trace Encoder (TRACE)

## GoBack

### 3.10 Registers

The addresses in this section are relative to RISC-V Trace Encoder base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

#### Register 3.1. TRACE_MEM_START_ADDR_REG (0x0000)

```
31                                 0
+---------------------------------------+
|               0x000000                |
+---------------------------------------+
```

TRACE_MEM_START_ADDR Configures the start address of the trace memory. (R/W)

#### Register 3.2. TRACE_MEM_END_ADDR_REG (0x0004)

```
31                                 0
+---------------------------------------+
|               0xffffffff              |
+---------------------------------------+
```

TRACE_MEM_END_ADDR Configures the end address of the trace memory. (R/W)

#### Register 3.3. TRACE_MEM_CURRENT_ADDR_REG (0x0008)

```
31                                 0
+---------------------------------------+
|               0x000000                |
+---------------------------------------+
```

TRACE_MEM_CURRENT_ADDR Represents the current memory address for writing. (RO)