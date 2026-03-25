

```markdown
## Register 4.4. mie (0x304)

IE Write 1 to enable the interrupt. (R/W)
```

```markdown
## Register 4.5. mtvec (0x305)

MODE Represents whether machine mode interrupts are vectored. Only vectored mode `0x1` is available. (RO)

BASE Configures the higher 24 bits of trap vector base address aligned to 256 bytes. (R/W)
```

```markdown
## Register 4.6. mscratch (0x340)

MSCRATCH Contains machine scratch information for custom use. (R/W)
```

```markdown
## Register 4.7. mepc (0x341)

MEPC Configures the machine trap/exception program counter. This is automatically updated with address of the instruction which was about to be executed while CPU encountered the most recent trap. (R/W)
```