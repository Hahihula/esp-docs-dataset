

# 20.8 Register Summary

The addresses in this section are relative to ECC Accelerator base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Interrupt Registers**<br><code>ECC_MULT_INT_RAW_REG</code> ECC raw interrupt status register<br><code>ECC_MULT_INT_ST_REG</code> ECC masked interrupt status register<br><code>ECC_MULT_INT_ENA_REG</code> ECC interrupt enable register<br><code>ECC_MULT_INT_CLR_REG</code> ECC interrupt clear register | 0x000C RO/WTC/SS<br>0x0010 RO<br>0x0014 R/W<br>0x0018 WT | |
| **Configuration Register**<br><code>ECC_MULT_CONF_REG</code> ECC configuration register | 0x001C varies | |
| **Version Register**<br><code>ECC_MULT_DATE_REG</code> Version control register | 0x00FC R/W | |