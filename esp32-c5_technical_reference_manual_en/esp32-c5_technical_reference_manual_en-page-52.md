

```markdown
| Name | Description | Address | Access |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------|:---------|:--------|
| **Machine Information CSRs** |  |  |  |
| mvendorid | Machine vendor ID | 0xF11 | RO |
| marchid | Machine architecture ID | 0xF12 | RO |
| mimpid | Machine implementation ID | 0xF13 | RO |
| mhartid | Machine hart ID | 0xF14 | RO |
| **Machine Trap Setup CSRs** |  |  |  |
| mstatus | Machine mode status | 0x300 | R/W |
| misa¹ | Machine ISA | 0x301 | R/W |
| mideleg | Machine interrupt delegation register (INACTIVE IN CLIC MODE) | 0x303 | RO |
| mie | Machine interrupt enable register (INACTIVE IN CLIC MODE) | 0x304 | RO |
| mtvec² | Machine trap vector | 0x305 | R/W |
| mcounteren | Machine counter enable | 0x306 | R/W |
| mtvt | Machine vector interrupt base address (Refer to CLIC specifications) | 0x307 | R/W |
| **Machine Trap Handling CSRs** |  |  |  |
| mscratch | Machine scratch | 0x340 | R/W |
| mepc | Machine trap program counter | 0x341 | R/W |
| mcause³ | Machine trap cause | 0x342 | R/W |
| mtval | Machine trap value | 0x343 | R/W |
| mip | Machine interrupt pending (INACTIVE IN CLIC MODE) | 0x344 | RO |
| mnxti | Interrupt handler address and enable modifier (Refer to CLIC specifications) | 0x345 | R/W |
| mintthresh | Interrupt threshold CSR (Refer to CLIC specifications) | 0x347 | RO |
| mintstatus | Current interrupt levels (Refer to CLIC specifications) | 0xFB1 | RO |
| mscratchcsw | Conditional scratch swap on priv mode change (Refer to CLIC specifications) | 0x348 | R/W |
| mscratchcswl | Conditional scratch swap on level change (Refer to CLIC specifications) | 0x349 | R/W |
| mclicbase | Machine mode interrupt controller base address register (CUSTOM) (Refer to CLIC specifications) | 0x350 | RO |
| **Physical Memory Protection (PMP) CSRs** |  |  |  |
| pmcfg0 | Physical memory protection configuration | 0x3A0 | R/W |
| pmcfg1 | Physical memory protection configuration | 0x3A1 | R/W |
| pmcfg2 | Physical memory protection configuration | 0x3A2 | R/W |
| pmcfg3 | Physical memory protection configuration | 0x3A3 | R/W |
| pmpaddrn (n: 0-15) | Physical memory protection address register | 0x3B0+0x1*n | R/W |
```