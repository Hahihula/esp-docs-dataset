

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.27. HP_SYSTEM_L2_MEM_INT_CLR_REG (0x00A8)
```

![HP_SYSTEM_L2_MEM_INT_CLR_REG bit field diagram](image_description: A 32-bit register with bits labeled as follows from right to left: Bit 0 is Reset; Bits 1–3 are reserved; Bit 4 corresponds to HP_SYSTEM_L2_MEM_ERR_RESP_INT_CLR; Bit 5 corresponds to HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_CLR; Bit 6 corresponds to HP_SYSTEM_L2_MEM_ECC_ERR_INT_CLR. The register name and bit labels are rotated diagonally across the diagram.)

```markdown
HP_SYSTEM_L2_MEM_ECC_ERR_INT_CLR Write 1 to clear L2_MEM_ECC_ERR_INT interrupt. (WT)

HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_CLR Write 1 to clear L2_MEM_EXCEED_ADDR_INT interrupt. (WT)

HP_SYSTEM_L2_MEM_ERR_RESP_INT_CLR Write 1 to clear L2_MEM_ERR_RESP_INT interrupt. (WT)
```

```markdown
Register 20.28. HP_SYSTEM_AHB2AXI_BRESP_ERR_INT_RAW_REG (0x0188)
```

![HP_SYSTEM_CPU_ICM_H2X_BRESP_ERR_INT_RAW bit field diagram](image_description: A 32-bit register with bits labeled as follows from right to left: Bit 0 is Reset; Bits 1–31 are reserved. The label "reserved" appears diagonally across the upper portion of the register, and a rotated diagonal label reads "HP_SYSTEM_CPU_ICM_H2X_BRESP_ERR_INT_RAW".)

```markdown
HP_SYSTEM_CPU_ICM_H2X_BRESP_ERR_INT_RAW The raw interrupt status of CPU_ICM_H2X_BRESP_ERR_INT, triggered when a BRESP error occurs in Post Write mode in AHB2AXI. (R/WTC/SS)
```

Espressif Systems

1272
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```