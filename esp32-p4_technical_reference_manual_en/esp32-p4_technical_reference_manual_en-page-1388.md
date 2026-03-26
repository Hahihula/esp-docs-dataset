
```markdown
Chapter 21 Debug Assistant

Register 21.65. ASSIST_DEBUG_CORE_1_RCD_EN_REG (0x00C4)

ASSIST_DEBUG_CORE_1_RCD_RECORDEN Configures whether to enable HP CPU1 PC logging.
O: Disable
1: ASSIST_DEBUG_CORE_1_RCD_PDEBUGPC_REG starts to record HP CPU1 PC in real time
(R/W)

ASSIST_DEBUG_CORE_1_RCD_PDEBUGEN Configures whether to enable HP CPU1 debugging.
O: Disable
1: HP CPU1 outputs HP CPU1 PC
(R/W)

Register 21.66. ASSIST_DEBUG_CORE_1_RCD_PDEBUGPC_REG (0x00C8)

ASSIST_DEBUG_CORE_1_RCD_PDEBUGPC Represents the PC value at HP CPU1 reset. (RO)
```