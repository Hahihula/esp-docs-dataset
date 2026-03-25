

```markdown\nChapter 16 Permission Control (PMS)\nGoBack\n\nRegister 16.45. CPU_APM_MO_EXCEPTION_INFO1_REG (0x00D4)\nCPU_APM_MO_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)\n\nRegister 16.46. CPU_APM_M1_STATUS_REG (0x00D8)\nCPU_APM_M1_EXCEPTION_STATUS Represents exception status.\nbit0: 1 represents permission restrictions\nbit1: 1 represents address out of bounds (RO)\n\nRegister 16.47. CPU_APM_M1_STATUS_CLR_REG (0x00DC)\nCPU_APM_M1_EXCEPTION_STATUS_CLR Write 1 to clear exception status. (WT)\n```
```