

```markdown
| Temporary disable JTAG 3 | EFUSE_DIS_USB_JTAG 4 | EFUSE_DIS_USB_SERIAL_JTAG 4 | EFUSE_DIS_PAD_JTAG 4 | EFUSE_JTAG_SEL_ENABLE 4 | Strapping Pin GPIO25 | USB_to_JTAG Status | PAD_to_JTAG Status |
|---------------------------|----------------------|------------------------------|-----------------------|--------------------------|----------------------|--------------------|--------------------|
| 0                         | 1                    | 1                            | 0                     | x                        | x                    | Unavailable        | Available          |
| 0                         | 0                    | 0                            | 1                     | x                        | x                    | Available          | Unavailable        |
| 0                         | 1                    | 0                            | 1                     | x                        | x                    | Unavailable        | Unavailable        |
| 0                         | 1                    | 1                            | 1                     | x                        | x                    | Unavailable        | Unavailable        |
| 1                         | x                    | x                            | x                     | x                        | x                    | Unavailable        | Unavailable        |

Note:
1. Available: the corresponding JTAG function is available.
   Unavailable: the corresponding JTAG function is not available.
2. x: do not care.
3. "Temporary disable JTAG" means that if there are an even number of bits "1" in EFUSE_SOFT_DIS_JTAG[2:0], the JTAG function is turned on (the corresponding value in the table is 1), otherwise it is turned off (the corresponding value in the table is 0). However, under certain special conditions of the HMAC Accelerator in ESP32-H2, the JTAG function may be turned on even if there is an odd number of bits "1" in EFUSE_SOFT_DIS_JTAG[2:0]. For information on how HMAC affects JTAG functionality, please refer to Chapter HMAC Accelerator.
4. Please refer to Chapter eFuse Controller to get more information about eFuse.
5. Please refer to Chip Boot Control to get more information about the strapping pin GPIO25.

1.10.5 Register Summary

Below is the list of Debug CSRs supported by ESP-RISC-V CPU core:

| Name         | Description                  | Address | Access |
|--------------|------------------------------|---------|--------|
| dcsr         | Debug Control and Status     | 0x7B0   | R/W    |
| dpc          | Debug PC                     | 0x7B1   | R/W    |
| dscratch0    | Debug Scratch Register 0     | 0x7B2   | R/W    |
| dscratch1    | Debug Scratch Register 1     | 0x7B3   | R/W    |

All the debug module registers are implemented in conformance to the specification RISC-V External Debug Support Version 0.13. Please refer to it for more details.

1.10.6 Register Description

Below are the details of Debug CSRs supported by ESP-RISC-V core:
```