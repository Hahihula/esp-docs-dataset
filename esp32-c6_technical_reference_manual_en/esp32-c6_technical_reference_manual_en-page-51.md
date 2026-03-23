

```markdown
Register 1.16. uie (0x004)

| Bit | Description |
|-----|-------------|
| 31:8 | UXIE[31:8] |
| 7-6 | reserved |
| 5-4 | UXIE[6:5] |
| 3 | UTIE |
| 2-1 | UXIEL[2:1] |
| 0 | USIE |

USIE Write 1 to enable the user software interrupt. (R/W)
UTIE Write 1 to enable the user timer interrupt. (R/W)
UXIE Write 1 to enable the 28 external interrupts delegated to U mode. (R/W)

Register 1.17. utvec (0x005)

| Bit | Description |
|-----|-------------|
| 31:24 | BASE |
| 7-6 | reserved |
| 5-0 | MODE |

MODE Represents if user mode interrupts are vectored. Only vectored mode 0x1 is available. (RO)
BASE Configures the higher 24 bits of trap vector base address aligned to 256 bytes. (R/W)

Register 1.18. uscratch (0x040)

| Bit | Description |
|-----|-------------|
| 31:0 | USCRATCH |

USCRATCH Configures user scratch information for custom use. (R/W)

Register 1.19. uepc (0x041)

| Bit | Description |
|-----|-------------|
| 31:0 | UEPC |

UEPC Configures the user trap program counter. This is automatically updated with address of the instruction which was about to be executed in User mode while CPU encountered the most recent user mode interrupt. (R/W)
```