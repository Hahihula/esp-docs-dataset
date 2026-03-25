

```markdown
Register 2.22. mcounteren (0x306)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 0                                                                             |
| 30-14| Reserved                                                                      |
| 13  | HPM13                                                                         |
| 12  | (reserved)                                                                    |
| 11  | HPM9                                                                          |
| 10  | HPM8                                                                          |
| 9   | (reserved)                                                                    |
| 8   | IR                                                                            |
| 7   | TM                                                                            |
| 6   | CY                                                                            |
| 5-3 | Reserved                                                                      |
| 2   | Reset                                                                         |
| 1   | 0                                                                             |
| 0   | 0                                                                             |

HPM13 Configures hpmcounter13 access from user mode.
O: Accessing hpmcounter13 CSR in user mode will generate illegal instruction exception.
1: Accessing hpmcounter13 CSR in user mode is valid.
(R/W)

HPM9 Configures hpmcounter9 access from user mode.
O: Accessing hpmcounter9 CSR in user mode will generate illegal instruction exception.
1: Accessing hpmcounter9 CSR in user mode is valid.
(R/W)

HPM8 Configures hpmcounter8 access from user mode.
O: Accessing hpmcounter8 CSR in user mode will generate illegal instruction exception.
1: Accessing hpmcounter8 CSR in user mode is valid.
(R/W)

CY Configures access of cycle counter from user mode.
O: Accessing cycle CSR in user mode will generate illegal instruction exception.
1: Accessing cycle CSR in user mode is valid.
(R/W)

TM Configures access of time counter from user mode.
O: Accessing time CSR in user mode will generate illegal instruction exception.
1: Accessing time CSR in user mode is valid.
(R/W)

IR Configures access of instret counter from user mode.
O: Accessing instret CSR in user mode will generate illegal instruction exception.
1: Accessing instret CSR in user mode is valid.
(R/W)
```