

```markdown
| ID | Description |
|----|-------------|
| 0-2 | NA (Reserved) |
| 3 | CLINT M mode software interrupt |
| 4-6 | NA (Reserved) |
| 7 | CLINT M mode timer interrupt |
| 8-15 | NA (Reserved) |
| 16 | External interrupt 0 |
| 17 | External interrupt 1 |
| 18 | External interrupt 2 |
| ... | ... |
| 45 | External interrupt 29 |
| 46 | External interrupt 30 |
| 47 | External interrupt 31 |

## Table 1.8-1. CLIC Interrupt Mapping

### 1.8.2.4 CLIC Parameters

The available features of a CLIC implementation can be discovered using the registers `mclicbase` and `clicinfo`:

*   `mclicbase` is a read-only CSR which holds the base address of the CLIC memory-mapped registers for machine mode.
*   `clicinfo` is a memory-mapped read-only register. It consists of the following fields:
    *   `NUM_INTERRUPTS`: Represents the number of interrupts supported by the current CLIC implementation
    *   `CLICINTCTLBITS`: Represents the number of programmable higher bits in `clicintctl[i]` and `mintthresh.TH` for encoding the level and priority of each interrupt

*   Once the value of the `mclicbase` is known, the full address of the `clicinfo` can be computed by adding the corresponding address offset of 0x0004 (shown in Section 1.8.2.6) to the `mclicbase` value.

### 1.8.2.5 Interrupt Level and Priority Encoding

Table 1.8-2 shows the possible ways that level and priority can be specified for CLIC interrupts, based on the configured values of `mcliccfg.MNLBITS` and `clicintctl[i]` registers, and the fixed value of the `CLICINTCTLBITS` parameter (0x3 for this CLIC implementation).
```