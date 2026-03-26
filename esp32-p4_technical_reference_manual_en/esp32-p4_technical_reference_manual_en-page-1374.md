

```markdown
Chapter 21 Debug Assistant

Register 21.43. ASSIST_DEBUG_CORE_O_RCD_EN_REG (0x0044)

ASSIST_DEBUG_CORE_O_RCD_RECORDEN Configures whether to enable HP CPU0 PC logging.
O: Disable
1: ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG starts to record HP CPU0 PC in real time
(R/W)

ASSIST_DEBUG_CORE_O_RCD_PDEBUGEN Configures whether to enable HP CPU0 debugging.
O: Disable
1: HP CPU0 outputs HP CPU0 PC
(R/W)

Register 21.44. ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG (0x0048)

ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC Represents the PC value at HP CPU0 reset. (RO)
```