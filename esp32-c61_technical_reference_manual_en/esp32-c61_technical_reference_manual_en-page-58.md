

```markdown
Register 1.32. mcounteren (0x306)

| Bit | Field Name | Description |
|-----|------------|-------------|
| 31  |            |             |
|     |            | HPM13       | (reserved) | HPM9        | HPM8        | (reserved) | IR          | TM          | CY          |
| 14  | 13         | 12          | 10          | 9           | 8           | 7           | 3           | 2           | 1           | 0           |
|     |            |             |             |             |             |             |             |             |             | Reset        |

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