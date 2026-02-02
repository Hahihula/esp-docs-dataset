**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**GoBack Link:** GoBack

---

### Section Heading:
Memory Management and Protection Units (MMU, MPU)

#### Subsection 4.1 Introduction
Every peripheral and memory section in the ESP32 is accessed through either an MMU or an MPU.

- **MMU/MPU**: Memory Unit that can allow or disallow access to a specific application's address range based on permissions given by OS.
- Applications use virtual-to-physical translation for internal/external addresses, allowing mapping and configuration adjustments per application needs. 
- Differentiates between the operating system (OS) and applications through Process Identifiers (PIDs).
- Each PID has its own set of mappings and rights.

#### Subsection 4.2 Features
- Eight processes in each PRO_CPU and APP_CPU.
- MPU/MMU manages on-chip memories, off-chip memories, peripherals based on process ID:
  - On-chip memory management by MPU/MMU
  - Off-chip memory management by MMU
  - Peripheral management by MPU

#### Subsection 4.3 Functional Description

##### Sub-subsection 4.3.1 PID Controller
In the ESP32, a PID controller signals which MMU/MPU owns running code.

- OS updates PID in PID controller when switching contexts.
- Detects interrupts and switches PIDs to another application if configured by OS (if applicable).

There are two peripheral PID controllers for each of the CPUs. Each allows different processes on CPU(s) as desired, enabling flexible multitasking or process management across multiple cores.

---

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback