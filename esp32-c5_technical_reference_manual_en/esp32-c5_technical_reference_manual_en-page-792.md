

```markdown
Register 18.89. TEE_TIMERGROUP0_CTRL_REG (0x00D4)
Register 18.90. TEE_TIMERGROUP1_CTRL_REG (0x00D8)
Register 18.91. TEE_SYSTIMER_CTRL_REG (0x00DC)
Register 18.92. TEE_PCNT_CTRL_REG (0x00F4)
Register 18.93. TEE_IOMUX_CTRL_REG (0x00F8)
Register 18.94. TEE_PSRAM_MEM_MONITOR_CTRL_REG (0x00FC)
Register 18.95. TEE_MEM_ACS_MONITOR_CTRL_REG (0x0100)
Register 18.96. TEE_HP_SYSTEM_REG_CTRL_REG (0x0104)
Register 18.97. TEE_PCR_REG_CTRL_REG (0x0108)
Register 18.98. TEE_MSPI_CTRL_REG (0x010C)
Register 18.99. TEE_HP_APM_CTRL_REG (0x0110)
Register 18.100. TEE_CPU_APM_CTRL_REG (0x0114)
Register 18.101. TEE_TEE_CTRL_REG (0x0118)
Register 18.102. TEE_CRYPT_CTRL_REG (0x011C)
Register 18.103. TEE_TRACE_CTRL_REG (0x0120)
Register 18.104. TEE_CPU_BUS_MONITOR_CTRL_REG (0x0128)
Register 18.105. TEE_INTPI_REG_CTRL_REG (0x012C)
Register 18.106. TEE_TWA1_CTRL_REG (0x0138)
Register 18.107. TEE_SPI2_CTRL_REG (0x013C)
Register 18.108. TEE_BS_CTRL_REG (0x0140)
Register 18.109. TEE_PERI_CTRL_REG (0x0088-0x0158)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | TEE_READ_TEE_PERI Configures the read permission of PERI in TEE mode. (R/W) |
| 29  | TEE_READ_REEO_PERI Configures the read permission of PERI in REEO mode. (R/W)|
| 28  | TEE_READ_REE1_PERI Configures the read permission of PERI in REE1 mode. (R/W)|
| 27  | TEE_READ_REE2_PERI Configures the read permission of PERI in REE2 mode. (R/W)|
| 26  | TEE_WRITE_TEE_PERI Configures the write permission of PERI in TEE mode. (R/W)|
| 25  | TEE_WRITE_REEO_PERI Configures the write permission of PERI in REEO mode. (R/W)|
| 24  | TEE_WRITE_REE1_PERI Configures the write permission of PERI in REE1 mode. (R/W)|
| 23  | TEE_WRITE_REE2_PERI Configures the write permission of PERI in REE2 mode. (R/W)|
```