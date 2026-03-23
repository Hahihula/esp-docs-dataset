

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG)
GoBack

Register 17.18: ASSIST_DEBUG_CORE_O_RCD_EN_REG (0x0044)

ASSIST_DEBUG_CORE_O_RCD_RECORDEN Set to 1 to enable ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG to record PC in real time. (R/W)

ASSIST_DEBUG_CORE_O_RCD_PDEBUGGEN Set to 1 to enable CPU debug function. The CPU outputs PC only when this field is set to 1. (R/W)

Register 17.19: ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG (0x0048)

ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC Records the PC value at CPU reset. (RO)
```