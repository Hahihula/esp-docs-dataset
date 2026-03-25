

```markdown
| Aspect          | TEE                                       | REE                          |
|-----------------|-------------------------------------------|-------------------------------|
| Security        | Enhanced security                         | Normal security               |
| Access permission | The master in TEE mode always has read, write, and execute permissions in the address range. | Different levels of access permissions are configurable by software. |

## 15.4 Functional Description

### 15.4.1 TEE Controller Functional Description

ESP32-H2 provides four security modes: TEE, REEO, REE1, and REE2.

For the CPU to access memory or peripheral registers, first select the machine mode or user mode of the CPU, then configure its security mode. For the configuration of machine mode and user mode, please refer to RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10.

* When the CPU is in machine mode, its security mode is TEE mode.
* When the CPU is in user mode, its security mode is REE mode. To specify REEO, REE1 or REE2 mode, `TEE_MO_MODE` of `TEE_MO_MODE_CTRL_REG` should be configured:
  - If `TEE_MO_MODE` is set to 0, which is TEE mode, the valid mode that actually takes effect in the CPU user mode is REEO.
  - if `TEE_MO_MODE` is set to 1, 2 or 3, which is in REE mode, its security mode is REEO, REE1 and REE2 respectively.

As for other masters, security mode can be set by configuring `TEE_Mn_MODE`. *n* here equals the ID number of master in Table 15.4-1.

Table 15.4-1. Master Access Source

| Value | Source                                                                 |
|-------|------------------------------------------------------------------------|
| 0     | CPU                                                                     |
| 1     | Reserved                                                                |
| 2     | Reserved                                                                |
| 3     | Reserved                                                                |
| 4     | Reserved                                                                |
| 5     | MEM_MONITOR                                                             |
| 6     | TRACE                                                                   |
| 7 ~ 15| Reserved                                                                |
| 16 ~ 31| See the peripherals corresponding to the values 0 ~ 15 in Chapter 3 GDMA Controller (GDMA) > Table 3.4-1 Selecting Peripherals via Register Configuration. For example, 16 corresponds to the peripheral with value 0 in that table, and 17 corresponds to the peripheral with value 1 in that table, and so on. |
```