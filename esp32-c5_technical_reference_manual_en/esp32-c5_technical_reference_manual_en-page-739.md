

```markdown
## 18.3 Features

ESP32-C5 has two TEE controllers: HP_TEE and LP_TEE.

*   **HP_TEE** has the following features:
    - Supports four security modes for the masters
    - Supports configurable security mode for 32 masters

*   **LP_TEE** has the following features:
    - Supports four security modes for the masters
    - Supports configurable security mode for one master (i.e., the LP CPU)

ESP32-C5 has four SYS_APM controllers: HP_APM_CTRL, LP_APM_CTRL, LP_APMO_CTRL, and CPU_APM_CTRL.

*   **HP_APM_CTRL** has the following features:
    - Supports access permission configuration for up to 16 address ranges
    - Supports access management to HP SRAM, HP CPU peripheral registers, HP system peripheral registers, and external memory
    - Interrupt function on illegal access
    - Exception information record

*   **LP_APM_CTRL** has the following features:
    - Supports access permission configuration for up to eight address ranges
    - Supports access management to LP SRAM (in low-speed mode) and LP peripheral registers
    - Interrupt function on illegal access
    - Exception information record

*   **LP_APMO_CTRL** has the following features:
    - Supports access permission configuration for up to eight address ranges
    - Supports access management to LP SRAM (in high-speed mode)
    - Interrupt function on illegal access
    - Exception information record

*   **CPU_APM_CTRL** has the following features:
```