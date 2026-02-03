**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Section Titles and Subsections with Content:**

### Section:
Table 15.6-2. Interrupt Registers for Unauthorized DBUS Access

| **Registers** | Bit | Description |
|----------------|-----|-------------|
| PMS_CORE_mDRAMO_PMS_MONITOR_1_REG | [0] | Clears interrupt signal |
| | [1] | Enables interrupt |
| | (0) | Stores interrupt status of unauthorized DBUS access |
| PMS_CORE_mDRAMO_PMS_MONITOR_2_REG | [1] | Flags atomic access. 1: atomic access; 0: not atomic access. |
| | **[3:2]** | Stores the world the CPU was in when the unauthorized DBUS access happened. Ob01: Secure World; Ob10: Non-secure World |
| PMS_CORE_mDRAMO_PMS_MONITOR_3_REG | [0] | Stores the access direction. 1: write; 0: read. |
| | **[25:4]** | Stores the byte information of the unauthorized DBUS access. |

### Section:
15.6.3 Interrupt upon Unauthorized Access to External Memory

**Body Text:**  
ESP32-S3 can be configured to trigger Interrupt upon unauthorized access to external memory, and log the information about this unauthorized access. This interrupt corresponds to the SPI_MEM_REJECT_INTR interrupt source described in Table 9.3-1 from Chapter 9 Interrupt Matrix (INTERRUPT).

### Section:
Table 15.6-3. Interrupt Registers for Unauthorized Access to External Memory

| **Registers** | Bit | Description |
|----------------|-----|-------------|
| SYSCON_SPI_MEM_PMSCTL_REG | [0] | Stores exception signal |
| | [1] | Clears exception signal and logged information |
| | (2) | Indicates unauthorized instruction execution |
| | (3) | Indicates unauthorized read |
| | (4) | Indicates unauthorized write |
| | **[5]** | Indicates overlapping split regions |
| | **[6]** | Indicates invalid address |

### Section:
15.6.4 Interrupt upon Unauthorized Access to Internal Memory via GDMA

**Body Text:**  
ESP32-S3 can be configured to trigger Interrupt upon unauthorized access to internal memory via GDMA, and log the information about this unauthorized access. This interrupt corresponds to the DMA_APB_PMS_MONITOR_VIOLATE_INTR interrupt source described in Table 9.3-1 from Chapter 9 Interrupt Matrix (INTERRUPT).

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)