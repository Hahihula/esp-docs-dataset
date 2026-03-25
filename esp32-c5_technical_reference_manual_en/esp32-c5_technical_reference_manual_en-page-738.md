

```markdown
Figure 18.1-1. PMP-APM Management Relation

The diagram illustrates that when the HP CPU accesses ROM and EXT_MEM, the access paths are solely managed by PMP. On the other hand, when the HP CPU accesses the other address spaces, the access paths are controlled by both PMP and APM. If the PMP check fails, the APM permission control will not be triggered.

For peripheral registers, there are two levels of APM permission control: the first level manages access permissions of address regions, and the second level manages access permissions of peripherals.

PMP-related registers are located inside the HP CPU and can be read or configured with special instructions.

For how to configure PMP, please refer to Chapter 2 High-Performance CPU > Standard Physical Memory Protection.

The following sections will provide a detailed introduction to the APM module including its features, functions, and configurations.

18.2 Introduction to APM

The APM module contains two parts: the TEE (Trusted Execution Environment) controller and the APM controller. Each module contains its own registers: TEE registers and APM registers.

*   The TEE controller configures the security mode of a particular master in ESP32-C5 (such as GDMA) to access memory or peripheral registers. It supports four security modes: TEE, REEO (Rich Execution Environment), REE1, and REE2.
*   The APM controller has two types: SYS_APM controller and PERI_APM controller. The registers of SYS_APM controller are in the APM registers, and the registers of PERI_APM controller are in the TEE registers.

    -   The SYS_APM controller manages a master’s access permissions when accessing memory and peripheral registers. By comparing the pre-configured address ranges and corresponding access permissions with the information carried on the bus, such as ID number (please refer to Table 18.5-1), security mode, access address, access permissions, etc., the SYS_APM controller determines whether the access is allowed.
    -   The PERI_APM controller manages the master’s access permissions to peripheral registers.
```