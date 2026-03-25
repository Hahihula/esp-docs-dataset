

```markdown
- Supports access permission configuration for up to eight address ranges
- Supports HP CPU’s access management to HP SRAM
- Interrupt function on illegal access
- Exception information record

ESP32-C5 has two PERI_APM controllers: HP_PERI_APM_CTRL and LP_PERI_APM_CTRL.

• HP_PERI_APM_CTRL and LP_PERI_APM_CTRL share the following features:
  - Support separate permission configuration for each peripheral register
  - Support returning error status to the master via the system bus
  - Exception information record

## 18.4 TEE and REE Terminology

TEE Stands for Trusted Execution Environment, which is a secure area that is isolated from the main operating system and provides a secure environment for executing sensitive operations.

REE Stands for Rich Execution Environment, which is the main operating system and environment in which most applications run.

Table 18.4-2. Comparison Between TEE and REE

| Aspect          | TEE                          | REE                                |
|-----------------|------------------------------|------------------------------------|
| Security        | Enhanced security            | Normal security                    |
| Access permission | Masters in TEE mode always have read, write, and execute permissions in the address range. | Different levels of access permissions of REEO/1/2 are configurable by software. |

## 18.5 Functional Description

### 18.5.1 TEE Controller Functional Description

ESP32-C5 supports four security modes: TEE, REEO, REE1, and REE2.

For the HP CPU to access memory or peripheral registers, first select the machine mode or user mode for it, then configure its security mode with HP_TEE registers. For the configuration of machine mode and user mode, please refer to RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10.

• When the HP CPU is in machine mode, its security mode is TEE mode.
• When the HP CPU is in user mode, its security mode is REE mode, defined by `TEE_MO_MODE` as follows:
  - If `TEE_MO_MODE` is 0, which is TEE mode, the valid mode that actually takes effect in the HP CPU user mode is REEO.
  - if `TEE_MO_MODE` is 1, 2, or 3, the security mode is REEO, REE1, and REE2 respectively.
```