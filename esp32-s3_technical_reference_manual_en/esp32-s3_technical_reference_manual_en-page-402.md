**Chapter Title:**
Chapter 4 System and Memory

**Body Text:**

Single-byte, double-byte, 4-byte, and 16-byte alignment. The CPU can also access data via the instruction bus but only in 4-byte aligned manner; non-aligned data access will cause a CPU exception.

The CPU can:
- directly access the internal memory via both data bus and instruction buses;
- directly access the external memory which is mapped into the address space via cache;
- directly access modules/peripherals via data bus.

**Figure Caption:**
Figure 4.2 lists the address ranges on the data bus and instruction bus and their corresponding target memory.

Some internal and external memory can be accessed via both data bus and instruction bus. In such cases, the CPU can access the same memory using multiple addresses.

**Subsection Title (with section number):**
4.3.2 Internal Memory

The ESP32-S3 consists of the following three types of internal memory:

- **Internal ROM (384 KB):** The internal ROM is a read-only memory and cannot be programmed. Internal ROM contains the ROM code (software instructions and some software read-only data) of some low-level system software.

- **Internal SRAM (512 KB):** The Internal Static RAM (SRAM) is a volatile memory that can be quickly accessed by the CPU (generally within a single CPU clock cycle).
  - A part of the SRAM can be configured to operate as a cache for external memory access, which cannot be accessed by CPU in such case.
  - Some parts of the SRAM can only be accessed via the CPU’s instruction bus.
  - Some parts of the SRAM can only be accessed via the CPU's data bus.
  - Some parts of the SRAM can be accessed via both the CPU’s instruction bus and the CPU’s data bus.

- **RTC Memory (16 KB):** The RTC (Real Time Clock) memory implemented as Static RAM (SRAM) and thus is volatile. However, RTC memory has the added feature of being persistent throughout deep sleep (i.e., the RTC memory retains its values throughout deep sleep).

  - **RTC FAST Memory (8 KB):** RTC FAST memory can only be accessed by the CPU, and cannot be accessed by the ULP co-processor. It is generally used to store instructions and data that needs to persist across a deep sleep.

  - **RTC SLOW Memory (8 KB):** The RTC SLOW memory can be accessed by both the CPU and the ULP co-processor, and thus is generally used to store instructions and share data between the CPU and the ULP co-processor.

Based on the three different types of internal memory described above, the internal memory of the ESP32-S3 is split into four segments: Internal ROM (384 KB), Internal SRAM (512 KB), RTC FAST Memory (8 KB) and RTC SLOW Memory (8 KB). However, within each segment, there may be different bus access restrictions (e.g., some parts of the segment may only be accessible by the CPU’s instruction bus). Therefore, some segments are also further divided down into parts. Table 4.3-1 describes each part of internal memory and their address ranges on the data bus and/or in instruction bus.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback