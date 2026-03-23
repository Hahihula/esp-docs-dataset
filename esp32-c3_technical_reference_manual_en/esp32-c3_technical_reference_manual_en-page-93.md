

```markdown
- directly access the internal memory via both data bus and instruction bus;
- access the external memory which is mapped into the virtual address space via cache;
- directly access modules/peripherals via data bus.

Figure 3.2-1 lists the address ranges on the data bus and instruction bus and their corresponding target memory.

Some internal and external memory can be accessed via both data bus and instruction bus. In such cases, the CPU can access the same memory using multiple addresses.
```

```markdown
## 3.3.2 Internal Memory

The ESP32-C3 consists of the following three types of internal memory:

- **Internal ROM (384 KB):** The Internal ROM of the ESP32-C3 is a Mask ROM, meaning it is strictly read-only and cannot be reprogrammed. Internal ROM contains the ROM code (software instructions and some software read-only data) of some low level system software.

- **Internal SRAM (400 KB):** The Internal Static RAM (SRAM) is a volatile memory that can be quickly accessed by the CPU (generally within a single CPU clock cycle).

  - A part of the SRAM can be configured to operate as a cache for external memory access.
  - Some parts of the SRAM can only be accessed via the CPU’s instruction bus.
  - Some parts of the SRAM can be accessed via both the CPU’s instruction bus and the CPU’s data bus.

- **RTC Memory (8 KB):** The RTC (Real Time Clock) memory implemented as Static RAM (SRAM) thus is volatile. However, RTC memory has the added feature of being persistent in deep sleep (i.e., the RTC memory retains its values throughout deep sleep).

  - RTC FAST Memory (8 KB): RTC FAST memory can only be accessed by the CPU and can be generally used to store instructions and data that needs to persist across a deep sleep.

Based on the three different types of internal memory described above, the internal memory of the ESP32-C3 is split into three segments: Internal ROM (384 KB), Internal SRAM (400 KB), RTC FAST Memory (8 KB).

However, within each segment, there may be different bus access restrictions (e.g., some parts of the segment may only be accessible by the CPU’s Data bus). Therefore, each some segments are also further divided into parts. Table 3.3-1 describes each part of internal memory and their address ranges on the data bus and/or instruction bus.
```

```markdown
Table 3.3-1. Internal Memory Address Mapping

| Bus Type       | Boundary Address Low Address | Boundary Address High Address | Size (KB) | Target                  |
|----------------|------------------------------|--------------------------------|-----------|-------------------------|
|                |                              |                                |           |                         |
| Data bus       | Ox3FF0_0000                   | Ox3FF1_FFFF                    | 128       | Internal ROM 1          |
|                | Ox3FC8_0000                   | Ox3FCD_FFFF                    | 384       | Internal SRAM 1         |
| Instruction bus| Ox4000_0000                   | Ox4003_FFFF                    | 256       | Internal ROM O          |
|                | Ox4004_0000                   | Ox4005_FFFF                    | 128       | Internal ROM 1          |
|                | Ox4037_C000                   | Ox4037_FFFF                    | 16        | Internal SRAM O         |

Cont’d on next page
```