

```markdown
Chapter 1 ESP-RISC-V CPU

DEBUG HOST
  Debugger (GDB) <--> Debug Translator (OPENOCD)
              <--> DEBUG TRANSPORT HARDWARE

ESP-RV CORE COMPLEX
DEBUG MODULE (DM)
  DM REG <-> DMI <-> JTAG DTM
RESET/HALT CONTROL <-> (to ESP-RV CORE components)
ABSTRACT_CMD/PROGRAM/BUFFER <-> (bidirectional to core debug structures)

ESP-RV CORE
  DEBUG MODE
  REG FILE
  HW TRIGGER

BUS ACCESS <-> SYSTEM BUS

Figure 1.10-1. Debug System Overview

The user interacts with the Debug Host (e.g. laptop), which is running a debugger (e.g. GDB). The debugger communicates with a Debug Translator (e.g. OpenOCD, which may include a hardware driver) to communicate with Debug Transport Hardware (e.g. ESP-Prog adapter). The Debug Transport Hardware connects the Debug Host to the HP core's Debug Transport Module (DTM) through standard JTAG interface. The DTM provides access to the Debug Module (DM) using the Debug Module Interface (DMI).

Espressif Systems
100
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```