

# Chapter 21 Debug Assistant

## Register 21.69. ASSIST_DEBUG_CORE_1_DEBUG_MODE_REG (0x00F4)

ASSIST_DEBUG_CORE_1_DEBUG_MODE Represents whether HP CPU1 is in debugging mode.
- 1: In debugging mode
- 0: Not in debugging mode  
(RO)

ASSIST_DEBUG_CORE_1_DEBUG_MODULE_ACTIVE Represents the status of the HP CPU1 debug module.
- 1: Active status
- Other: Inactive status  
(RO)

## Register 21.70. ASSIST_DEBUG_CLOCK_GATE_REG (0x0108)

ASSIST_DEBUG_CLK_EN Configures whether to enable the register clock gating.
- 0: Disable
- 1: Enable  
(R/W)