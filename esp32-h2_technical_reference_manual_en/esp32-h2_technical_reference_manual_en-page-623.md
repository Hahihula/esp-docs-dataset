

```markdown
Chapter 21 HMAC Accelerator (HMAC)
GoBack

21.5 Registers

The addresses in this section are relative to HMAC Accelerator base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 21.1. HMAC_SET_START_REG (0x0040)

HMxAC_SET_START Configures whether to enable HMxAC.
O: Disable HMxAC
1: Enable HMxAC
(WO)

Register 21.2. HMAC_SET_PARA_FINISH_REG (0x004C)

HMxAC_SET_PARA_END Configures whether to finish HMxAC configuration.
O: No effect
1: Finish configuration
(WO)

Register 21.3. HMAC_SET_MESSAGE_CALC_BLOCK_REG (0x0050)

HMxAC_SET_TEXT_ONE Calls SHA to calculate one message block. (WO)
```