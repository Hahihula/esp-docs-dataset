

```markdown
Register 1.7. mideleg (0x303)

MIDELEG Configures the U mode delegation state for each interrupt ID. Below interrupts are delegated to U mode by default:
Bit 0: User software interrupt (CLINT)
Bit 4: User timer interrupt (CLINT)
Bit 8: User external interrupt
The default delegation can be modified at run-time if required.
(R/W)

Register 1.8. mie (0x304)

USIE Write 1 to enable the user software interrupt. (R/W)
MSIE Write 1 to enable the machine software interrupt. (R/W)
UTIE Write 1 to enable the user timer interrupt. (R/W)
MTIE Write 1 to enable the machine timer interrupt. (R/W)
MXIE Write 1 to enable the 28 external interrupts. (R/W)

Register 1.9. mtvec (0x305)

MODE Represents whether machine mode interrupts are vectored. Only vectored mode 0x1 is available. (RO)
BASE Configures the higher 24 bits of trap vector base address aligned to 256 bytes. (R/W)
```