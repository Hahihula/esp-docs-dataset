

```markdown
| EFUSE_DIS_USB_JTAG 3 | EFUSE_DIS_USB_SERIAL_JTAG 3 | EFUSE_DIS_PAD_JTAG 3 | EFUSE_JTAG_SEL_ENABLE 3 | Strapping Pin GPIO7 4 | USB JTAG Status | PAD JTAG Status |
|----------------------|------------------------------|-----------------------|--------------------------|------------------------|-----------------|------------------|
|                      |                              |                       |                          |                        |                 |                  |
| 0                    | 0                            | 0                     | 0                        | x 2                    | Available       | Unavailable      |
|                      |                              |                       |                          |                        | 1               | 1                |
| 0                    | 0                            | 0                     | 1                        | 1                      | Available       | Unavailable      |
|                      |                              |                       |                          |                        |                 |                  |
| 0                    | 0                            | 0                     | 1                        | 0                      | Unavailable     | Available        |
| 0                    | 1                            | 0                     | x                        | x                      | Unavailable     | Available        |
| 1                    | 0                            | 0                     | x                        | x                      | Unavailable     | Available        |
| 1                    | 1                            | 0                     | x                        | x                      | Unavailable     | Available        |
|                      |                              |                       |                          |                        |                 |                  |
| 0                    | 0                            | 1                     | x                        | x                      | Available       | Unavailable      |
| 0                    | 1                            | 1                     | x                        | x                      | Unavailable     | Unavailable      |
| 1                    | 0                            | 1                     | x                        | x                      | Unavailable     | Unavailable      |
| 1                    | 1                            | 1                     | x                        | x                      | Unavailable     | Unavailable      |

Note:
1. Available: the corresponding JTAG function is available.
Unavailable: the corresponding JTAG function is not available.
2. x: do not care.
3. Please refer to Chapter eFuse Controller to get more information about eFuse.
4. Please refer to Chip Boot Control to get more information about the strapping pin GPIO7.

1.10.1.5 Register Summary

Below is the list of Debug CSRs supported by HP core:

| Name         | Description                          | Address | Access |
|--------------|--------------------------------------|---------|--------|
| dcsr         | Debug Control and Status Register    | 0x7B0   | R/W    |
| dpc          | Debug PC Register                    | 0x7B1   | R/W    |
| dscratch0    | Debug Scratch Register 0             | 0x7B2   | R/W    |
| dscratch1    | Debug Scratch Register 1             | 0x7B3   | R/W    |

All the debug module registers are implemented in conformance to the specification RISC-V External Debug Support Version 0.13.2. Please refer to it for more details.

1.10.1.6 Register Description

Below are the details of Debug CSRs supported by HP core:
```