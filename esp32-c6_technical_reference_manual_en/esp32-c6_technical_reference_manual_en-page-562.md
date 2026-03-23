

```markdown
Chapter 16 Permission Control (PMS)

Figure 16.1-1. PMP-APM Management Relation

PMP related registers are located inside HP CPU and can be read or configured by special instructions. For how to configure PMP, please refer to chapter High-Performance CPU > Physical Memory Protection.

APM module contains two parts: TEE (Trusted Execution Environment) controller and APM controller. Each of them contains its own register module: TEE register module and APM register module.

* The TEE controller is responsible for configuring the security mode of a particular master in ESP32-C6 (such as DMA, which can access memory as a master). There are four types of security mode: TEE, REEO (Rich Execution Environment), REE1, REE2.
* The APM controller is responsible for managing a master’s access permissions (read/write/execute) when accessing memory and peripheral registers. By comparing the pre-configured address ranges and corresponding access permissions with the information carried on the bus, such as ID number (please refer to the table 18.4-5 in Chapter 18 Debug Assistant (ASSIST_DEBUG)), security mode, access address, access permissions, etc., APM determines whether access is allowed.

TEE related registers are used to configure the security mode of each master, and the APM related registers are used to specify the access permission and access address range of each security mode. With TEE controller and APM controller, ESP32-C6 can precisely control the access permission of all masters to memory and peripheral registers.

16.2 Features

ESP32-C6’s TEE controller has the following features:

* Four security modes available for the masters
* Security mode configuration for up to 32 masters

ESP32-C6’s APM controller has the following features:

* Access permission configuration for up to 16 address ranges
* Access management to internal and external memory and peripheral registers
* Interrupt function
* Exception information record
```