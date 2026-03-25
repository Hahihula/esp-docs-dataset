

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)
GoBack

Register 17.30. ASSIST_DEBUG_CORE_O_RCD_EN_REG (0x0044)

ASSIST_DEBUG_CORE_O_RCD_RECORDEN Configures whether to enable PC logging.
O: Disable
1: ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG starts to record PC in real time
(R/W)

ASSIST_DEBUG_CORE_O_RCD_PDEBUGEN Configures whether to enable CPU debugging.
O: Disable
1: CPU outputs PC
(R/W)

Register 17.31. ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG (0x0048)

ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC Represents the PC value at CPU reset. (RO)
```