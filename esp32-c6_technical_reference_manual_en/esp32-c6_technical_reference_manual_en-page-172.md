

```markdown
LP SRAM can be accessed by the following modes:

* high-speed mode, i.e., the LP SRAM is accessed in HP CPU clock frequency. In this case:
  - HP CPU can access the LP SRAM without any latency.
  - But the latency of LP CPU accessing LP SRAM ranges from a few dozen to dozens of LP CPU cycles.

* low-speed mode, i.e., the LP SRAM is accessed in LP CPU clock frequency. In this case:
  - LP CPU can access the LP SRAM with zero cycle latency.
  - But the latency of HP CPU accessing LP SRAM ranges from a few dozen to dozens of HP CPU cycles.

You can switch the modes based on your application scenarios.

* If the LP CPU is not working, you can switch to high-speed mode to improve the access speed of the HP CPU.
* If the LP CPU is executing code in the LP SRAM, you can switch to the low-speed mode.

When the HP CPU is in sleep mode, you must switch to the low-speed mode.

Detailed configuration is as follows:

* Configure `LP_AON_FAST_MEM_MUX_SEL` to select the mode needed:
  - 1: high-speed mode
  - 0: low-speed mode

* Set `LP_AON_FAST_MEM_MUX_SEL_UPDATE` to start mode switch.

* Read `LP_AON_FAST_MEM_MUX_SEL_STATUS` to check if mode switch is done:
  - 0: mode is switched
  - 1: mode is not switched


## 5.3.3 External Memory

ESP32-C6 supports SPI, Dual SPI, Quad SPI, and QPI interfaces that allow connection to external flash. ESP32-C6 also supports hardware manual encryption and automatic decryption based on XTS-AES algorithm to protect users' programs and data in the external flash.

### 5.3.3.1 External Memory Address Mapping

The HP CPU accesses the external memory via the cache. According to information inside the MMU (Memory Management Unit), the cache maps the HP CPU's address (`0x4200_0000 ~ 0x42FF_FFFF`) into a physical address of the external memory. Due to this address mapping, ESP32-C6 can address up to 16 MB external flash. Note that the instruction bus shares the same address space (16 MB) with the data bus to access the external memory.
```