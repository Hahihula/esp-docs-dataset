

```markdown
## 1.10 Debug

### 1.10.1 Overview

This section describes how to debug and test software running on ESP-RISC-V core. Debug support is provided through standard JTAG pins and complies to RISC-V External Debug Support Specification version 0.13.

Figure 1.10-1 below shows the main components of External Debug Support.

![Figure 1.10-1. Debug System Overview](image_path)

The user interacts with the Debug Host (e.g., laptop), which is running a debugger (e.g., gdb). The debugger communicates with a Debug Translator (e.g., OpenOCD, which may include a hardware driver) to communicate with Debug Transport Hardware (e.g., ESP-Prog adapter). The Debug Transport Hardware connects the Debug Host to the ESP-RISC-V Core’s Debug Transport Module (DTM) through a standard JTAG interface. The DTM provides access to the Debug Module (DM) using the Debug Module Interface (DMI).

The DM allows the debugger to halt selected cores. Abstract commands provide access to GPRs (general purpose registers). The Program Buffer allows the debugger to execute arbitrary code on the core, which allows access to additional CPU core state. Alternatively, additional abstract commands can provide access to additional CPU core state. ESP-RISC-V core contains Trigger Module supporting 4 triggers. When trigger
```