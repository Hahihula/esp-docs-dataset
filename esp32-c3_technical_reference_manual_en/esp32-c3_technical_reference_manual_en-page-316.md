

```markdown
Chapter 14 Permission Control (PMS)

GoBack

Figure 14.1-1. Permission Control Overview

For details about PMP, please refer to Section 1.8.1 in Chapter 1 ESP-RISC-V CPU. For details about World Controller, please refer to Chapter 15 World Controller (WCL). This chapter only describes ESP32-C3's PMS mechanism.

14.2 Features

ESP32-C3’s extended permission control mechanism supports:

* Independent access management in a privileged environment and unprivileged environment
* Independent access management to internal memory, including
    - CPU access to internal memory
    - GDMA access to internal memory
* Independent access management to external memory, including
    - CPU to external memory via SPI1
    - CPU to external memory via Cache
* Independent access management to peripheral regions, including
    - CPU access to peripheral regions
    - Interrupt upon unsupported access alignment
* Address splitting for more flexible access management
* Register locks to secure the integrity of access management related registers
* Interrupt upon unauthorized access

14.3 Privileged Environment and Unprivileged Environment

During PMS check, ESP32-C3 chip:

* When in the privileged environment: check the permission configuration registers for the privileged environment
```