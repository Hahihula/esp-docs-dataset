

# 2.10 Debug and Trace Support

## 2.10.1 Debug

### 2.10.1.1 Overview

This section describes how to debug software running on HP and LP CPU cores. Debug support is provided through standard JTAG pins and complies to the [RISC-V External Debug Support Version 0.13.2](#) specification.

HP core and LP core have their own dedicated JTAG DTM (debug transport module) in order to connect with respective Debug Modules. Both these JTAG DTMs are daisy-chained to provide debugger access to respective cores via a single JTAG interface. Depending on its debug requirements, Debugger can keep the unused DTM in a bypass state while debugging the required core. The HP core can be debugged through a single debug module (DM) connected to JTAG DTM (HP Core), while the LP core is debugged through a separate debug module (DM) connected to JTAG DTM (LP Core).

Please note it is not possible to debug the HP core and the LP core at the same time as they are accessed through separate debug modules.

Figure 2.10-1 below shows the main components of External Debug Support.

![Figure 2.10-1. Debug System Overview](image)

**Figure 2.10-1. Debug System Overview**

Espressif Systems

Submit Documentation Feedback