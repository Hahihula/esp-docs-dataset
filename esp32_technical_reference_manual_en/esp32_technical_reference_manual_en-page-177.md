**Title: ESP32 TRM (Version 5.6)**

---

### Table of Contents:

1. **Peripheral Interrupt Configuration Register**
   - **Columns:** 
     - Bit
     - Status Register Name
     - No.
     - Name
     - No.

2. **Peripheral Interrupt Source**
   - Similar structure to the first table, but for different interrupt sources (e.g., APP_CPU).

---

### Table: Peripheral Interrupt Configuration Register

| Bit | Status Register Name       | No.  | Name      |
|-----|-------------------------------|------|-----------|
|     |                             |      |           |
| 21  | DPORT_PRO_SPI2_DMA_INT_MAP_REG | S3   | SPI2_DMA_INT | 54 |
| 22  | DPORT_PRO_SPI3_DMA_INT_MAP_REG | S4   | SPI3_DMA_INT | 54 |
| 23  | DPORT_PRO_WDG_INT_MAP_REG     | S5   | WDG_INT    | 55 |
| 24  | DPORT_PRO_TIMER_INT_MAP_REG   | S6   | TIMER_INT   | 55 |
| 25  | DPORT_PRO_TIMER_INT2_MAP_REG  | S7   | TIMER_INT2  | 57 |
| 26  | DPORT_PRO_TG_TO_EDGE_INT_MAP_REG | S8   | TG_TO_EDGE_INT | 57 |
| 27  | DPORT_PRO_TG_TO TILE_EDGE_INT_MAP_REG | S9   | TGToTILE_EDGE_INT | 57 |
| 28  | DPORT_PRO_WDT_EDGE_INT_MAP_REG | S10  | WDT_EDGE_INT | 60 |
| 29  | DPORT_PRO_LACT_EDGE_INT_MAP_REG | S11  | LACT_EDGE_INT | 61 |
| 30  | DPORT_PRO_TGT_TO_EDGE_INT_MAP_REG | S12  | TGToEDGE_INT | 62 |
| 31  | DPORT_PRO_TG1_TO TILE_EDGE_INT_MAP_REG | S13  | TG1ToTILE_EDGE_INT | 63 |
| 32  | DPORT_PRO_WDT_EDGE_INT_MAP_REG | S14  | WDT_EDGE_INT | 65 |
| 33  | DPORT_PRO_LACT_EDGE_INT_MAP_REG | S15  | LACT_EDGE_INT | 67 |
| 34  | DPORT_PRO_MMU_IA_INT_MAP_REG   | S8   | MMU_IA_INT  | 68 |

---

### Table: Peripheral Interrupt Source

- Similar structure to the first table, but for different interrupt sources (e.g., APP_CPU).

---

**Note:** The tables continue with similar structures and entries. Each row in both tables corresponds to a specific bit number of an interrupt configuration register or source name along with its corresponding status register numbers.

---

### Footer:
- Page Number: 177
- Document Feedback Link

---