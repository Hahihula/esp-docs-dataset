

```markdown
| Aspect     | TEE                                      | REE                                       |
|------------|------------------------------------------|-------------------------------------------|
| Security   | Enhanced security                        | Normal security                           |
| Access permission | Masters in TEE mode always have read, write, and execute permissions in the address range. | Different levels of access permissions of REEO/1/2 are configurable by software. |

## 16.5 Functional Description

### 16.5.1 TEE Controller Functional Description

ESP32-C61 supports four security modes: TEE, REEO, REE1, and REE2.

For the HP CPU to access memory or peripheral registers, first select the machine mode or user mode for it, then configure its security mode with HP_TEE registers. For the configuration of machine mode and user mode, please refer to RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10.

- When the HP CPU is in machine mode, its security mode is TEE mode.
- When the HP CPU is in user mode, its security mode is REE mode. The specific REEO, REE1 or REE2 mode depends on `TEE_MO_MODE` as follows:
  - If `TEE_MO_MODE` is 0, which is TEE mode, the valid mode that actually takes effect in the HP CPU user mode is REEO.
  - if `TEE_MO_MODE` is set to 1, 2, or 3, the security mode is REEO, REE1, and REE2 respectively.

For masters other than the HP CPU to access memory or peripheral registers, configure their security mode with `TEE_Mn_MODE`. `n` represents the ID number of master as listed in Table 16.5-1.

Table 16.5-1. Master Access Source from HP System

| Value of n | Source     |
|------------|------------|
| 0          | HP CPU     |
| 1          | Reserved   |
| 2          | Reserved   |
| 3          | Reserved   |
```