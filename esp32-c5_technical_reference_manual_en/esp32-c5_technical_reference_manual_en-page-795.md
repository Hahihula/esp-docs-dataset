

```markdown
## Register 18.128. LP_TEE_PERI_CTRL_REG (0x0004-0x004C)

LP_TEE_READ_TEE_PERI Configures the read permission of PERI in TEE mode. (R/W)
LP_TEE_READ_REEO_PERI Configures the read permission of PERI in REEO mode. (R/W)
LP_TEE_READ_REE1_PERI Configures the read permission of PERI in REE1 mode. (R/W)
LP_TEE_READ_REE2_PERI Configures the read permission of PERI in REE2 mode. (R/W)

LP_TEE_WRITE_TEE_PERI Configures the write permission of PERI in TEE mode. (R/W)
LP_TEE_WRITE_REEO_PERI Configures the write permission of PERI in REEO mode. (R/W)
LP_TEE_WRITE_REE1_PERI Configures the write permission of PERI in REE1 mode. (R/W)
LP_TEE_WRITE_REE2_PERI Configures the write permission of PERI in REE2 mode. (R/W)

## Register 18.129. LP_TEE_FORCE_ACC_HP_REG (0x0090)

LP_TEE_FORCE_ACC_HPMEM_EN Configures whether to allow LP CPU to forcibly access HP SRAM regardless of permission management.
0: Disable force access to HP SRAM
1: Enable force access to HP SRAM
(R/W)
```