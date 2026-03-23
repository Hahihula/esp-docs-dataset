

```markdown
- When not in the unprivileged environment: check the permission configuration registers for the unprivileged environment
```

Users can choose either of these two ways below to enter the chip into privileged environment:

- By configuring the world controller  
  - Switching to Secure world: entering the privileged environment  
  - Switching to Non-secure world: entering the unprivileged environment

- By configuring the privileged level of the 32-bit RISC-V CPU:  
  - Switching to Machine mode: entering the privileged environment  
  - Switching to User mode: entering the unprivileged environment

Users can configure `PMS_PRIVILEGE_MODE_SEL` to choose between the above-mentioned two ways to enter the chip into privileged environment:

- 0 (Default): via configuring the world controller. See details in Chapter 15 World Controller (WCL).
- 1: via configuring the CP's privileged level. See details in Chapter 1 ESP-RISC-V CPU.

The following sections introduce how to configure the permission to different areas in the privileged environment and the unprivileged environment.

## 14.4 Internal Memory

ESP32-C3 has the following types of internal memory:

- ROM: 384 KB in total, including 256 KB Internal ROM0 and 128 KB Internal ROM1
- SRAM: 400 KB in total, including 16 KB Internal SRAM0 and 384 KB Internal SRAM1
- RTC FAST Memory: 8 KB in total, which can be further split into two regions each with independent permission configuration

This section describes how to configure the permission to each type of ESP32-C3's internal memory.

### 14.4.1 ROM

ESP32-C3's ROM can be accessed by CPU's instruction bus (IBUS) and data bus (DBUS) when configured. The ROM ranges accessible for IBUS and DBUS respectively are listed in Table 14.4-1.

Table 14.4-1. ROM Address

<table><thead><tr><th rowspan="2">ROM</th><th colspan="2">IBUS Address</th><th colspan="2">DBUS Address</th></tr><tr><th>Starting Address</th><th>Ending Address</th><th>Starting Address</th><th>Ending Address</th></tr></thead><tbody><tr><td>Internal ROM0</td><td>0x4000_0000</td><td>0x4003_FFFF</td><td>-</td><td>-</td></tr><tr><td>Internal ROM1</td><td>0x4004_0000</td><td>0x4005_FFFF</td><td>0x3FF0_0000</td><td>0x3FF1_FFFF</td></tr></tbody></table>

ESP32-C3 uses the registers listed in Table 14.4-2 to configure the instruction execution (X), write (W) and read (R) accesses of CPU's IBUS and DBUS, in User mode and Machine mode. Note that access configuration to ROM0 and ROM1 cannot be configured separately:
```