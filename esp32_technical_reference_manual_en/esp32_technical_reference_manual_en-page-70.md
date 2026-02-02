**Chapter 3: System and Memory**

---

### **3.3.2.6 DMA**

DMA uses the same addressing as the CPU data bus to read and write Internal SRAM 1 and Internal SRAM 2.
This means DMA uses an address range of `0x3FFE_0000 ~ 0x3FFF_FFFF` to read and write Internal SRAM 1
and an address range of `0x3FFA_E000 ~ 0x3FFD_FFFF` to read and write Internal SRAM 2.

In the ESP32, 13 peripherals are equipped with DMA. Table **3.3-3** lists these peripherals.
| Module | UARTO | UART1 | UART2 |
|--------|-------|-------|-------|
| SPI    | SPI1  | SPI2  | SPI3  |
| I/O    | I2S0  | I2S1  |
| SDIO Slave | SDMMC |
| EMAC   |

---

### **3.3.2.7 RTC FAST Memory**

RTC FAST Memory is 8 KB of SRAM. It can be read and written by PRO_CPU only at an address range of `0x3FF8_0000 ~ 0x3FF8_1FFF` on the data bus or at a address range of `0x400C_0000 ~ 0x400C_1FFF` on the instruction bus. Unlike most other memory regions, RTC FAST memory cannot be accessed by the APP_CPU.

The two address ranges of PRO_CPU access RTC FAST Memory in the same order, so for example, addresses `0x3FF8_0000` and `0x400C_0000` do not provide access to RTC FAST Memory or any other memory location on the APP_CPU.

---

### **3.3.2.8 RTC SLOW Memory**

RTC SLOW Memory is 8 KB of SRAM which can be read and written by either CPU at an address range of `0x5000_0000 ~ 0x5000_1FFF`. This address range is shared by both the data bus and the instruction bus.

---

### **3.3.3 External Memory**

The ESP32 can access external SPI flash and SPI SRAM as external memory. Table **3.3-4** provides a list of external memories that can be accessed by either CPU at a range of addresses on the data and instruction buses.
When a CPU accesses external memory through the Cache and MMU, the cache will map the CPU’s address to an external physical memory address (in the external memory's address space), according to the MMU settings. Due to this address mapping, the ESP32 can address up to 16 MB External Flash and 8 MB External SRAM.

| Bus Type | Low Address | Boundary Address | High Address | Size | Target | Comment |
|----------|-------------|------------------|--------------|------|-------|---------|
| Data     | `0x3F40_0000` | `0x3F7F_FFFF`    |              | 4 MB | External Flash | Read |

---

**Espressif Systems**

**ESP32 TRM (Version 5.6)**

[Submit Documentation Feedback](#)