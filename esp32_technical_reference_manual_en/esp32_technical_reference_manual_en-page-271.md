**Chapter Title:**
Chapter 13

**Section Heading:**
Process ID Controller (PID)

**Subsection 13.1 Overview**

The ESP32 is a dual core device and is capable of running and managing multiple processes. The PID Controller supports switching of PID when a process switch occurs. In addition to PID management, the PID Controller also facilitates management of nested interrupts by recording execution status just before an interrupt service routine is executed. This enables the user application to manage process switches and nested interrupts more efficiently.

**Subsection 13.2 Features**

The PID Controller features:
- Process management and priority
- Process PID switch
- Interrupt information recording
- Nested interrupt management

**Subsection 13.3 Functional Description**

Eight processes run on the CPU, and are assigned with PID of 0 ~ 7 respectively. Among the eight processes, processes with PID of 0 or 1 are elevated processes with higher authority compared to processes with PID ranging from 2 ~ 7.

A CPU process switch may occur in two cases:
- An interrupt occurs and the CPU fetches an instruction from the interrupt vector. Instruction fetch or execution from interrupt vector is always treated as a process with PID of 0, irrespective of which process was being executed on the CPU when the interrupt occurred.
- A currently active process explicitly performs a process switch. Only elevated processes with PID of 0 or 1 may perform a process switch.

**Subsection 13.3.1 Interrupt Identification**

Interrupts are classified into seven priority levels: Level 1, Level 2, Level 3, Level 4, Level 5, Level 6 (Debug), and NMI. Each level of interrupt is assigned an interrupt vector entry address. The PID Controller recognizes CPU instruction fetch from an interrupt vector entry address and automatically switches PID to 0. If CPU only accesses the interrupt vector entry address, PID Controller performs no action.

**Footer:**
Espressif Systems
271

**Link Texts:**
- Submit Documentation Feedback
- ESP32 TRM (Version 5.6)
- GoBack