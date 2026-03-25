
```markdown
## 16.2 Introduction to APM

The APM module contains two parts: the TEE (Trusted Execution Environment) controller and the APM controller. Each module contains its own register: the TEE register and APM register.

* The TEE controller is responsible for configuring the security mode of a particular master in ESP32-C61 (such as GDMA) to access memory or peripheral registers. There are four security modes: TEE, REEO (Rich Execution Environment), REE1, and REE2.
* The APM controller manages a master’s access permissions when accessing memory and peripheral registers. By comparing the pre-configured address ranges and corresponding access permissions with the information carried on the bus, such as ID number (please refer to Table 16.5-1), security mode, access address, access permissions, etc., the APM controller determines whether the access is allowed.

TEE-related registers configure the security mode of each master. The APM-related registers specify the access permission and access address range of each master in the configured security mode. With the TEE controller and APM controller, ESP32-C61 can precisely control the access permission of all masters to the memory and peripheral registers.

## 16.3 Features

ESP32-C61 has one TEE controller: HP_TEE.

* HP_TEE has the following features:
    - Four security modes for the masters
    - Configurable security mode for 32 masters

ESP32-C61 has three APM controllers: HP_APM_CTRL, LP_APM_CTRL, and CPU_APM_CTRL.

* HP_APM_CTRL has the following features:
    - Access permission configuration for up to 16 address ranges
    - Access management to HP SRAM, HP CPU_PERI, HP_PERI, and EXT MEM
    - Interrupt function on illegal access
    - Exception information record

* LP_APM_CTRL has the following features:
    - Access permission configuration for up to four address ranges
    - Access permission management to LP_PERI
    - Interrupt function on illegal access
    - Exception information record

* CPU_APM_CTRL has the following features:
    - Access permission configuration for up to eight address ranges
    - Access permission management for HP CPU to access HP SRAM
    - Interrupt function on illegal access
```