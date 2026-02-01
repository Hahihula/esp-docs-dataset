Title: Functional Description

- GDMA
- CPU through Cache

Subtitle: Manage access to peripherals, supporting
- independent permission control for each peripheral
- monitoring non-aligned access
- access control for customized address range

Subtitle: Integrate permission lock register
- All permission registers can be locked with the permission lock register. Once locked, the permission register and the lock register cannot be modified, unless the CPU is reset.

Subtitle: Integrate permission monitor or interrupt
- In case of illegitimate access, the permission monitor interrupt will be triggered and the CPU will be informed to handle the interrupt.
For details, see [ESP32-S3 Technical Reference Manual > Chapter Permission Control](#).

---

Title: 4.1.3.11 World Controller

Body Text:
ESP32-S3 can divide the hardware and software resources into a Secure World and a Non-Secure World to prevent sabotage or access to device information. Switching between the two worlds is performed by the World Controller.

Subtitle: Feature List
- Control of the CPU switching between secure and non-secure worlds
- Control of 15 DMA peripherals switching between secure and non-secure worlds
- Record of CPU’s world switching logs
- Shielding of the CPU’s NMI interrupt

For details, see [ESP32-S3 Technical Reference Manual > Chapter World Controller](#).

---

Title: 4.1.3.12 System Registers

Body Text:
ESP32-S3 system registers can be used to control the following peripheral blocks and core modules:

- System and memory
- Clock
- Software Interrupt
- Low-power management
- Peripheral clock gating and reset
- CPU Control

For details, see [ESP32-S3 Technical Reference Manual > Chapter System Registers](#).

Footer:
Espressif Systems  
47  
[Submit Documentation Feedback](#)  
ESP32-S3 Series Datasheet v2.1