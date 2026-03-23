

```markdown
| Target                                 | Boundary Address      | Size (KB) | Notes |
|----------------------------------------|-----------------------|-----------|-------|
|                                        | Low Address           | High Address |       |
| Digital Signature                      | 0x6003_D000           | 0x6003_DFFF   | 4     |
| HMAC Accelerator                       | 0x6003_E000           | 0x6003_EFFF   | 4     |
| GDMA Controller                         | 0x6003_F000           | 0x6003_FFFF   | 4     |
| ADC Controller                          | 0x6004_0000           | 0x6004_0FFF   | 4     |
| Reserved                                |                       |             |       |
|                                        | 0x6004_1000           | 0x6002_FFFF   |       |
| USB Serial/JTAG Controller              | 0x6004_3000           | 0x6004_3FFF   | 4     |
| Reserved                                | 0x6004_4000           | 0x600B_FFFF   |       |
| System Registers                        | 0x600C_0000           | 0x600C_0FFF   | 4     |
| PMS Registers                           | 0x600C_1000           | 0x600C_1FFF   | 4     |
| Interrupt Matrix                        | 0x600C_2000           | 0x600C_2FFF   | 4     |
| Reserved                                | 0x600C_3000           | 0x600C_3FFF   |       |
| Reserved                                | 0x600C_4000           | 0x600C_BFFF   |       |
| External Memory Encryption and Decryption | 0x600C_C000           | 0x600C_CFFF   | 4     |
| Reserved                                | 0x600C_D000           | 0x600C_DFFF   |       |
| Assist Debug                            | 0x600C_E000           | 0x600C_EFFF   | 4     |
| Reserved                                | 0x600C_F000           | 0x600C_FFFF   |       |
| World Controller                        | 0x600D_0000           | 0x600D_0FFF   | 4     |
```