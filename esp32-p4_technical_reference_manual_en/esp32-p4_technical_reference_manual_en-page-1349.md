

```markdown
## 21.7 Registers

The addresses of HP CPU bus logging configuration registers (see 21.6.1) in this section are relative to the SPM Monitor base address. The addresses of DMA bus logging configuration registers (see 21.6.2) in this section are relative to the L2MEM Monitor base address. The addresses of other registers (see 21.7.3) are relative to the Bus Monitor base address. All base addresses are provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### 21.7.1 HP CPU Bus Logging Configuration Registers

Register 21.1. SPM_MEM_MONITOR_LOG_SETTING_REG (0x0000)

SPM_MEM_MONITOR_LOG_MODE Configures monitoring modes.
bit[0]: Configures write monitoring.
O: Disable
1: Enable
bit[1]: Configures word monitoring.
O: Disable
1: Enable
bit[2]: Configures halfword monitoring.
O: Disable
1: Enable
bit[3]: Configures byte monitoring.
O: Disable
1: Enable
(R/W)

SPM_MEM_MONITOR_LOG_MEM_LOOP_ENABLE Configures the writing mode for recorded data.
1: Loop mode
O: Non-loop mode
(R/W)

Continued on the next page...
```