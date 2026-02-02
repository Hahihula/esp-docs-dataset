**Title: Chapter 27 SD/MMC Host Controller (SDHOST)**

**Table of Registers**

| Name           | Description                                      | Address       | Access |
|----------------|--------------------------------------------------|---------------|--------|
| TCBCNT_REG    | Transferred byte count register                  | 0x005C        | RO     |
| TBBCNT_REG    | Transferred byte count register                  | 0x0060        | RO     |
| DEBNCE_REG    | Debounce filter time configuration register      | 0x0064        | R/W    |
| USRID_REG     | User ID (scratchpad) register                   | 0x0068        | R/W    |
| RST_N_REG     | Card reset register                              | 0x0078        | R/W    |
| BMOD_REG      | Burst mode transfer configuration register       | 0x0080        | R/W    |
| PLDMND_REG    | Poll demand configuration register               | 0x0084        | WO     |
| DBADDR_REG    | Descriptor base address register                  | 0x0088        | R/W    |
| IDSTS_REG     | IDMAC status register                             | 0x008C        | R/W    |
| IDINTEN_REG   | IDMAC interrupt enable register                  | 0x0090        | R/W    |
| DSCADDR_REG   | Host descriptor address pointer                   | 0x0094        | RO     |
| BUFADDR_REG   | Host buffer address pointer register              | 0x0098        | RO     |
| CLK_EDGE_SEL  | Clock phase selection register                   | 0x0800        | R/W    |

**Section Title: 27.14 Registers**

SD/MMC controller registers can be accessed by the APB bus of the CPU.

The addresses in this section are relative to the SD/MMC base address provided in Table **3.3-6** in Chapter [3 System and Memory](#).

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

---

*Footer:*

Espressif Systems  
ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)