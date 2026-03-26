

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.25. HP_SYSTEM_L2_MEM_INT_ST_REG (0x00A0)

| Bit | Description |
|-----|-------------|
| 31-0 | reserved |

HP_SYSTEM_L2_MEM_ECC_ERR_INT_ST The masked interrupt status of L2_MEM_ECC_ERR_INT. (RO)
HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_ST The masked interrupt status of L2_MEM_EXCEED_ADDR_INT. (RO)
HP_SYSTEM_L2_MEM_ERR_RESP_INT_ST The masked interrupt status of L2_MEM_ERR_RESP_INT. (RO)

Register 20.26. HP_SYSTEM_L2_MEM_INT_ENA_REG (0x00A4)

| Bit | Description |
|-----|-------------|
| 31-0 | reserved |

HP_SYSTEM_L2_MEM_ECC_ERR_INT_ENA Write 1 to enable L2_MEM_ECC_ERR_INT interrupt. (R/W)
HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_ENA Write 1 to enable L2_MEM_EXCEED_ADDR_INT interrupt. (R/W)
HP_SYSTEM_L2_MEM_ERR_RESP_INT_ENA Write 1 to enable L2_MEM_ERR_RESP_INT interrupt. (R/W)

Espressif Systems
1271
Submit Documentation Feedback
ESP32-P4 TRM PRELIMINARY
```