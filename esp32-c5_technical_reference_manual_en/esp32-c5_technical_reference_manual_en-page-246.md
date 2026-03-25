

```markdown
| Target | Boundary Address Low Address | High Address | Size (KB) |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------|:--------------|:-----------|
| Memory Access Monitor 2<br>(PSARM_MEM_MONITOR)² | 0x6001_A000 | 0x6001_AFFF | 4 |
| Reserved | 0x6001_B000 | 0x6007_FFFF | |
| General DMA Controller (GDMA) | 0x6008_0000 | 0x6008_0FFF | 4 |
| General Purpose SPI2 Controller (GP-SPI2) | 0x6008_1000 | 0x6008_1FFF | 4 |
| Bit-scrambler (BITSCRAMBLER) | 0x6008_2000 | 0x6008_2FFF | 4 |
| Reserved | 0x6008_3000 | 0x6008_6FFF | |
| Key Manager | 0x6008_7000 | 0x6008_7FFF | 4 |
| AES Accelerator (AES) | 0x6008_8000 | 0x6008_8FFF | 4 |
| SHA Accelerator (SHA) | 0x6008_9000 | 0x6008_9FFF | 4 |
| RSA Accelerator (RSA) | 0x6008_A000 | 0x6008_AFFF | 4 |
| ECC Accelerator (ECC) | 0x6008_B000 | 0x6008_BFFF | 4 |
| Digital Signature (DS) | 0x6008_C000 | 0x6008_CFFF | 4 |
| HMAC Accelerator (HMAC) | 0x6008_D000 | 0x6008_DFFF | 4 |
| ECDSA Accelerator (ECDSA) | 0x6008_E000 | 0x6008_EFFF | 4 |
| Reserved | 0x6008_F000 | 0x6008_FFFF | |
| IO MUX | 0x6009_0000 | 0x6009_0FFF | 4 |
| GPIO Matrix | 0x6009_1000 | 0x6009_1FFF | 4 |
| Memory Access Monitor 1<br>(TCM_MEM_MONITOR)² | 0x6009_2000 | 0x6009_2FFF | 4 |
| Reserved | 0x6009_3000 | 0x6009_4FFF | |
| High-Performance System Registers<br>(HP_SYSREG) | 0x6009_5000 | 0x6009_5FFF | 4 |
| Power/Clock/Reset Registers (PCR) | 0x6009_6000 | 0x6009_6FFF | 4 |
| Reserved | 0x6009_7000 | 0x6009_7FFF | |
| Trusted Execution Environment (TEE)² | 0x6009_8000 | 0x6009_8FFF | 4 |
| High-Performance Access Permission Management<br>(HP_APM) | 0x6009_9000 | 0x6009_97FF | 2 |
| Low-Power Access Permission Management<br>(LP_APMO) | 0x6009_9800 | 0x6009_9FFF | 2 |
| CPU Access Permission Management<br>(CPU_APM) | 0x6009_A000 | 0x6009_AFFF | 4 |
| Reserved | 0x6009_B000 | 0x600A_FFFF | |
| Power Management Unit (PMU) | 0x600B_0000 | 0x600B_03FF | 1 |
| Low-Power Clock/Reset Registers<br>(LP_CLKRST) | 0x600B_0400 | 0x600B_07FF | 1 |
| Reserved | 0x600B_0800 | 0x600B_0BFF | |
| Low-Power Timer (LP_TIMER) | 0x600B_0C00 | 0x600B_0FFF | 1 |
| Low-Power Always-on Registers (LP_AON) | 0x600B_1000 | 0x600B_13FF | 1 |
| Low-Power UART (LP_UART) | 0x600B_1400 | 0x600B_17FF | 1 |
| Low-Power I2C (LP_I2C) | 0x600B_1800 | 0x600B_1BFF | 1 |
```