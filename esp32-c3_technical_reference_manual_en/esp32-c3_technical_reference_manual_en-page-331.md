

```markdown
| Registers | Bit | Description |
|:------------------------------------------------------------------|:-----|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PMS_CORE_O_PIF_PMS_MONITOR_1_REG | [1] | Enables interrupt<br>[0] Clears interrupt signal and logged information |
|  | [7:6] | Stores the privileged mode the CPU was in when the unauthorized PIF access happened. Ob01: privileged environment; Ob10: unprivileged environment |
|  | [5] | Stores the access direction. 1: write; 0: read |
| PMS_CORE_O_PIF_PMS_MONITOR_2_REG | [4:2] | Stores the data type of unauthorized access. 0: byte; 1: half-word; 2: word |
|  | [1] | Stores the access type. 0: instruction; 1: data |
|  | [0] | Stores the interrupt signal |
| PMS_CORE_O_PIF_PMS_MONITOR_3_REG | [31:0] | Stores the address of unauthorized access |

## 14.7.6 Interrupt upon Unauthorized PIF Access Alignment

Access to all of ESP32-C3's modules/peripherals is word aligned.

ESP32-C3 can be configured to check the access alignment to all modules/peripherals, and trigger Interrupt upon non-word aligned access.

This interrupt corresponds to the PMS_PERI_VIO_SIZE_INTR interrupt source described in Table 8.3-1 from Chapter 8 Interrupt Matrix (INTERRUPT).

Note that CPU can convert some non-word aligned access to word aligned access, thus avoiding triggering alignment interrupt.

Table 14.7-6 below lists all the possible access alignments and their results (when the interrupt is enabled), in which:

*   INTR: interrupt
*   √: access succeeds and no interrupt.
```