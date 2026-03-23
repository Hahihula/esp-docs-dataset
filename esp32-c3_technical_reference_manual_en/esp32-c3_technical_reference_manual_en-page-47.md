

```markdown
Chapter 1 ESP-RISC-V CPU

GoBack

1.6 Debug

1.6.1 Overview

This section describes how to debug and test software running on CPU core. Debug support is provided through standard JTAG pins and complies to RISC-V External Debug Support Specification version 0.13.

Figure 1.6-1 below shows the main components of External Debug Support.

![Figure 1.6-1. Debug System Overview](unrenderable_diagram)
```
```mermaid
graph TD
    DEBUG_HOST[DEBUG HOST] --> Debugger(GDB)
    Debugger[Debugger (GDB)] ↔ Debug_Translator[Debug Translator (OPENOCD)]
    Debug_Translator[Debug Translator (OPENOCD)] ↔ DEBUG_TRANSPORT_Hardware[DEBUG TRANSPORT HARDWARE]
    
    ESP_RV_CORE_COMPLEX[ESP-RV CORE COMPLEX] --> Debug_Module(DM)[DEBUG MODULE (DM)]
    Debug_Module(DM) ↔ DM_REG[DM REG]
    Debug_Module(DM) ↔ RESET_HALT_CONTROL[RESET/HALT CONTROL]
    Debug_Module(DM) ↔ Abstract_CMD_Program_Buffer[ABSTRACT_CMD/PROGRAM BUFFER]
    Debug_Module(DM) ↔ BUS_ACCESS[BUS ACCESS]
    
    DEBUG_TRANSPORT_Hardware[DEBUG TRANSPORT HARDWARE] ↔ JTAG_DTM[JTAG DTM]
    
    ESP_RV_CORE Complex[ESP-RV CORE] --> Debug_Mode[DEBUG MODE]
    ESP_RV_CORE Complex[ESP-RV CORE] --> REG_FILE[REG FILE]
    ESP_RV_CORE Complex[ESP-RV CORE] --> HW_TRIGGER[HW TRIGGER]
    
    BUS_ACCESS[BUS ACCESS] ↔ SYSTEM_BUS[SYSTEM BUS]
```
The user interacts with the Debug Host (eg. laptop), which is running a debugger (eg. gdb). The debugger communicates with a Debug Translator (eg. OpenOCD, which may include a hardware driver) to communicate with Debug Transport Hardware (eg. Olimex USB-JTAG adapter). The Debug Transport Hardware connects the Debug Host to the ESP-RV Core’s Debug Transport Module (DTM) through standard JTAG interface. The DTM provides access to the Debug Module (DM) using the Debug Module Interface (DMI).

The DM allows the debugger to halt the core. Abstract commands provide access to its GPRs (general purpose registers). The Program Buffer allows the debugger to execute arbitrary code on the core, which allows access to additional CPU core state. Alternatively, additional abstract commands can provide access to additional CPU core state. ESP-RV core contains Trigger Module supporting 8 triggers. When trigger conditions are met, cores will halt spontaneously and inform the debug module that they have halted.

System bus access block allows memory and peripheral register access without using RISC-V core.
```