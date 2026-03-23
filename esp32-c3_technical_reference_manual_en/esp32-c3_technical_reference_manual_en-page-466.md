

```markdown
Register 17.20. ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP_REG (0x004C)

ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP    Records SP. (RO)


Register 17.21. ASSIST_DEBUG_LOG_SETTING_REG (0x0070)

ASSIST_DEBUG_LOG_ENA   Enables the CPU bus or DMA bus access logging. bit[0]: CPU bus access logging; bit[1]: reserved; bit[2]: DMA bus access logging. (R/W)

ASSIST_DEBUG_LOG_MODE  Configures monitoring mode. bit[0]: write monitoring; bit[1]: word monitoring; bit[2]: halfword monitoring; bit[3]: byte monitoring. (R/W)

ASSIST_DEBUG_LOG_MEM_LOOP_ENABLE   Configures the writing mode for recorded data. 1: loop mode; 0: non-loop mode. (R/W)
```