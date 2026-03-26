

```markdown
- Read the value of HP_SYSTEM_SPM_INIT_DONE.
- Once HP_SYSTEM_SPM_INIT_DONE reaches a value of 1, set HP_SYSTEM_HP_SPM_PARITY_CHECK_EN to start parity check.
- (Recommended) clear HP_SYSTEM_SPM_INIT_EN and set HP_SYSTEM_SPM_INIT_CNT_RESET after HP_SYSTEM_SPM_INIT_CNT_RESET reaches 1 to complete the initialization process.

During the above process, avoid any access to HP SPM.


### 7.3.3 External Memory

ESP32-P4 supports SPI, dual SP, quad SPI and QPI interfaces for connecting to external flash, as well as OPI and HPI interfaces for connecting to external RAM.

ESP32-P4 provides the following security features to protect users' data in external flash and RAM:

- hardware manual encryption and automatic decryption based on XTS-AES algorithm to protect users' programs and data stored in the external flash.
- automatic encryption and decryption based on XTS-AES algorithm to protect users' data in the external RAM.

#### 7.3.3.1 External Memory Address Mapping

HP CPU can access external flash or RAM via `0x4000_0000 ~ 0x43FF_FFFF` or via `0x4800_0000 ~ 0x4BFF_FFFF` using cache-able or noncache-able methods. HP CPU can also access external flash or RAM directly via `0x8000_0000 ~ 0x83FF_FFFF` or via `0x8800_0000 ~ 0x8BFF_FFFF`, which is slower than the access via cache and is therefore commonly used for debugging.

When the HP CPU accesses external memory, it maps the addresses to physical addresses based on the information in the Memory Management Unit (MMU).

- Range (`0x4000_0000 ~ 0x43FF_FFFF`) is mapped to the physical address of the external flash accessed by HP CPU via cache.
- Range (`0x4800_0000 ~ 0x4BFF_FFFF`) is mapped to the physical address of the external RAM accessed by HP CPU via cache.
- Range (`0x8000_0000 ~ 0x83FF_FFFF`) is mapped to the physical address of the external flash accessed by HP CPU directly.
- Range (`0x8800_0000 ~ 0x8BFF_FFFF`) is mapped to the physical address of the external RAM accessed by HP CPU directly.

This mapping allows ESP32-P4 to address up to 64 MB of external flash and 64 MB of external RAM. **Note** that the instruction bus shares the same address space (64 MB) with the data bus for accessing external memory.

#### 7.3.3.2 Cache

As shown in Figure 7.3-3, ESP32-P4 has a two-level cache system, with the following features:

- L1 cache, including:
    - 16 KB of instruction cache (icache) with a 64 B block size, four-way set associative
```