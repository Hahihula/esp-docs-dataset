

```markdown
Chapter 15 Permission Control (PMS)

GoBack

PMP related registers are located inside the CPU and can be read or configured with special instructions. For how to configure PMP, please refer to Chapter ESP-RISC-V CPU > Section Physical Memory Protection.

The following sections of this chapter will describe the functions and configurations of the APM module.

The APM module contains two parts: the TEE (Trusted Execution Environment) controller and the APM controller. Each of them contains its own register module: TEE register module and APM register module.

* The TEE controller is responsible for configuring the security mode of a particular master in ESP32-H2 (such as GDMA) to access memory or peripheral registers. There are four security modes: TEE, REEO (Rich Execution Environment), REE1, and REE2.
* The APM controller is responsible for managing a master’s access permissions (read/write/execute) when accessing memory and peripheral registers. By comparing the pre-configured address ranges and corresponding access permissions with the information carried on the bus, such as ID number (please refer to Table 15.4-1), security mode, access address, access permissions, etc., the APM controller determines whether access is allowed.

TEE related registers are used to configure the security mode of each master, and the APM related registers are used to specify the access permission and access address range of each security mode. With TEE controller and APM controller, ESP32-H2 can precisely control the access permission of all masters to memory and peripheral registers.

15.2 Features

ESP32-H2’s TEE controller has the following features:

* Four security modes available for the masters
* Security mode configuration for up to 32 masters

ESP32-H2’s APM controller has the following features:

* Access permission configuration for up to 16 address ranges
* Access management to internal memory and peripheral registers
* Interrupt function on illegal access
* Exception information record

15.3 TEE and REE Terminology

TEE Stands for Trusted Execution Environment, which is a secure area that is isolated from the main operating system and provides a secure environment for executing sensitive operations.

REE Stands for Rich Execution Environment, which is the main operating system and environment in which most applications run.
```