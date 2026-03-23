

```markdown
Chapter 16 Permission Control (PMS)
GoBack

16.3 Functional Description

16.3.1 TEE Controller Functional Description

ESP32-C6 provides four kinds of security mode: TEE, REEO, REE1, and REE2.

For the HP CPU to access memory or peripheral registers, first select the machine mode or user mode of the
HP CPU, then configure its security mode. For the configuration of machine mode and user mode, please
refer to RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10.

- When the HP CPU is in machine mode, its security mode is TEE mode.
- When the HP CPU is in user mode, its security mode is REE mode. To specify REEO, REE1 or REE2
mode, TEE_MO_MODE of TEE_MO_MODE_CTRL_REG should be configured:
    - If set TEE_MO_MODE to 0, which is in TEE mode, its security mode is REEO.
    - If set TEE_MO_MODE to 1,2 or 3, which is in REE mode, its security mode is REEO, REE1 and REE2
respectively.

For the LP CPU’s access to memories or peripheral registers, security mode can be set by configuring the
LP_TEE_MO_MODE of LP_TEE_MO_MODE_CTRL_REG register.

As for other masters, security mode can be set by configuring the TEE_Mn_MODE of TEE registers. n here
equals to the ID number of master in table 18.4-5.

16.3.2 APM Controller Functional Description

16.3.2.1 Architecture

There are 3 register modules for APM registers:

- High Performance APM Registers (HP_APM_REG)
- Low Power APMO Registers (LP_APMO_REG)
- Low Power APM Registers (LP_APM_REG)

Figure 16.3-1 shows the access path managed by the APM controller.
```