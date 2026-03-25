

# 7.5 Registers

## 7.5.1 PCR Registers

The addresses in this section are relative to the Power/Clock/Reset (PCR) Register base address provided in Table 4.3-2 in Chapter 4 System and Memory.

### Register 7.1: PCR_UART0_CONF_REG (0x0000)

```
31                                 3   2   1   0
+-----------------------------------------------+
| PCR_UART0_CLK_EN | PCR_UART0_RST_EN | PCR_UART0_READY |
+-----------------------------------------------+
(reserved)
```

**PCR_UART0_CLK_EN** Configures whether or not to enable APB_CLK for UART0.  
- 0: Not enable  
- 1: Enable  
(R/W)

**PCR_UART0_RST_EN** Configures whether or not to reset UART0.  
- 0: Not reset  
- 1: Reset  
(R/W)

**PCR_UART0_READY** Represents whether or not UART0 is released from reset.  
- 0: Not released  
- 1: Released  
(RO)