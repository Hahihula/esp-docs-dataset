

```markdown
## 14.7.3 Interrupt upon Unauthorized Access to External Memory

ESP32-C3 can be configured to trigger Interrupt upon unauthorized access to external memory, and log the information about this unauthorized access. This interrupt corresponds to the `SPI_MEM_REJECT_INTR` interrupt source described in Table 8.3-1 from Chapter 8 Interrupt Matrix (INTERRUPT).

Table 14.7-3. Interrupt Registers for Unauthorized Access to External Memory

| Registers | Bit | Description |
|-----------|-----|-------------|
| SYSCON_SPI_MEM_PMS_CTRL_REG | [0] | Stores exception signal |
|  | [1] | Clears exception signal and logged information |
|  | [2] | Indicates unauthorized instruction execution |
|  | [3] | Indicates unauthorized read |
|  | [4] | Indicates unauthorized write |
|  | [5] | Indicates overlapping split regions |
|  | [6] | Indicates invalid address |

## 14.7.4 Interrupt upon Unauthorized Access to Internal Memory via GDMA

ESP32-C3 can be configured to trigger Interrupt upon unauthorized access to internal memory via GDMA, and log the information about this unauthorized access. This interrupt corresponds to the `PMS_DMA_VIO_INTR` interrupt source described in Table 8.3-1 from Chapter 8 Interrupt Matrix (INTERRUPT).

Table 14.7-4. Interrupt Registers for Unauthorized Access to Internal Memory via GDMA

| Registers | Bit | Description |
|-----------|-----|-------------|
| PMS_DMA_APBPERI_PMS_MONITOR_1_REG | [0] | Clears interrupt signal |
|  | [1] | Enables interrupt |
| PMS_DMA_APBPERI_PMS_MONITOR_2_REG | [0] | Stores interrupt signal |
|  | [2:1] | Stores the privileged mode the CPU was in when the unauthorized access happened. Ob01: privileged environment; Ob10: unprivileged environment |
|  | [24:3] | Stores the address that GDMA was trying to access unauthorized |
| PMS_DMA_APBPERI_PMS_MONITOR_3_REG | [0] | Stores the access direction. 1: write; 0: read |
|  | [16:1] | Stores the byte information of unauthorized access |

For information about Interrupt upon unauthorized access to external memory via GDMA, please refer to Chapter 2 GDMA Controller (GDMA).

## 14.7.5 Interrupt upon Unauthorized peripheral bus (PIF) Access

ESP32-C3 can be configured to trigger interrupts when PIF attempts to access RTC FAST memory and peripheral regions without configured permission, and log the information about this unauthorized access. Note that, once this interrupt is enabled, it’s enabled for all RTC FAST memory and peripheral regions, and
```