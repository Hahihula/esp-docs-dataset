

```markdown
| Name                     | Description                                                                                      | Address   | Access |
|--------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Machine Trap Handling CSRs** |                                                                                                  |           |        |
| mscratch                 | Machine scratch                                                                                  | 0x340     | R/W    |
| mepc                     | Machine trap program counter                                                                     | 0x341     | R/W    |
| mcause³                  | Machine trap cause                                                                               | 0x342     | R/W    |
| mtval                    | Machine trap value                                                                                | 0x343     | R/W    |
| mip                      | Machine interrupt pending (INACTIVE IN CLIC MODE)                                                | 0x344     | RO     |
| mnxti                    | Interrupt handler address and enable modifier (Refer to CLIC specifications)                     | 0x345     | R/W    |
| mintstatus               | Current interrupt levels (Refer to CLIC specifications)                                          | 0xFB1     | RO     |
| mintthresh               | Interrupt threshold (Refer to CLIC specifications)                                               | 0x347     | R/W    |
| mscratchcsw              | Conditional scratch swap on priv mode change (Refer to CLIC specifications)                      | 0x348     | R/W    |
| mscratchcswl             | Conditional scratch swap on level change (Refer to CLIC specifications)                          | 0x349     | R/W    |
| mclicibase               | Machine mode interrupt controller base address register (CUSTOM) (Refer to CLIC specifications)   | 0x350     | RO     |
| **User Trap Setup CSRs**  |                                                                                                  |           |        |
| ustatus                  | User mode status                                                                                 | 0x000     | R/W    |
| utvec⁴                   | User trap vector                                                                                | 0x005     | R/W    |
| uvt                      | User vector interrupt base address (Refer to CLIC specifications)                                | 0x007     | R/W    |
| **User Trap Handling CSRs** |                                                                                                  |           |        |
| uscratch                 | User scratch                                                                                    | 0x040     | R/W    |
| uepc                     | User trap program counter                                                                        | 0x041     | R/W    |
| ucause⁵                  | User trap cause                                                                                 | 0x042     | R/W    |
| unxti                    | Interrupt handler address and enable modifier (Refer to CLIC specifications)                     | 0x045     | R/W    |
| uintthresh               | Interrupt threshold (Refer to CLIC specifications)                                               | 0x047     | R/W    |
| uclibase                 | User mode interrupt controller base address (CUSTOM) (Refer to CLIC specifications)              | 0x050     | RO     |
| uintstatus               | Current interrupt levels (Refer to CLIC specifications)                                          | 0xCB1     | RO     |
| **Physical Memory Protection (PMP) CSRs** |                                                                                                  |           |        |
| pmpcfg0                  | Physical memory protection configuration                                                        | 0x3A0     | R/W    |
| pmpcfg1                  | Physical memory protection configuration                                                        | 0x3A1     | R/W    |
| pmpcfg2                  | Physical memory protection configuration                                                        | 0x3A2     | R/W    |
| pmpcfg3                  | Physical memory protection configuration                                                        | 0x3A3     | R/W    |
| pmpcfg4                  | Physical memory protection configuration                                                        | 0x3A4     | R/W    |
| pmpcfg5                  | Physical memory protection configuration                                                        | 0x3A5     | R/W    |
| pmpcfg6                  | Physical memory protection configuration                                                        | 0x3A6     | R/W    |
| pmpcfg7                  | Physical memory protection configuration                                                        | 0x3A7     | R/W    |
```