

```markdown
Figure 4.3-2. Modules/peripherals that can work with GDMA

These modules/peripherals can access any memory available to GDMA. For more information, please refer to Chapter 3 GDMA Controller (GDMA).

Note:
When accessing a memory via GDMA, a corresponding access permission is needed, otherwise this access may fail.
For more information about permission control, please refer to Chapter 15 Permission Control (PMS).

4.3.5 Modules/Peripherals Address Mapping

Table 4.3-2 lists all the modules/peripherals and their respective address ranges. Note that the address space of specific modules/peripherals is defined by “Boundary Address” (including both Low Address and High Address).

Table 4.3-2. Module/Peripheral Address Mapping
```

```markdown
| Target                                      | Boundary Address         | Size (KB) |
|---------------------------------------------|--------------------------|-----------|
|                                             | Low Address              | High Address   |           |
| UART Controller 0 (UART0)                   | 0x6000_0000              | 0x6000_OFFF    | 4         |
| UART Controller 1 (UART1)                   | 0x6000_1000              | 0x6000_1FFF    | 4         |
| External Memory Encryption and Decryption   | 0x6000_2000              | 0x6000_2FFF    | 4         |
| (XTS_AES)                                   |                          |               |           |
| Reserved                                    | 0x6000_3000              | 0x6000_3FFF    |           |
| I2C Controller 0 (I2CO)                     | 0x6000_4000              | 0x6000_4FFF    | 4         |
| I2C Controller 1 (I2C1)                     | 0x6000_5000              | 0x6000_5FFF    | 4         |
| UHCI Controller (UHCI)                      | 0x6000_6000              | 0x6000_6FFF    | 4         |

Cont’d on next page
```