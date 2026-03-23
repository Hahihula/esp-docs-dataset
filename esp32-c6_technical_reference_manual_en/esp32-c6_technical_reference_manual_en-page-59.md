

```markdown
Software may also update the value of INTPRI_COREO_CPU_INT_THRESH_REG and program MIE=1 for allowing higher priority interrupts to preempt the current ISR (nesting). However, before doing so, all the state CSRs must be saved (mepc, mstatus, mcause, etc.) since they will get overwritten due to occurrence of such an interrupt. Later, when exiting the ISR, the values of these CSRs must be restored.

Finally, after the execution returns from the ISR back to the trap handler, MRET instruction is used to resume normal execution.

Later, if the n interrupt is no longer needed and needs to be disabled, the following sequence may be followed:

1. save the state of MIE and clear MIE to 0
2. check if the interrupt is pending in INTPRI_COREO_CPU_INT_EIP_STATUS_REG
3. set/unset the nth bit of INTPRI_COREO_CPU_INT_ENABLE_REG
4. if the interrupt is of edge type and was found to be pending in step 2 above, nth bit of INTPRI_COREO_CPU_INT_CLEAR_REG must be toggled, so that its pending status gets flushed
5. execute FENCE instruction
6. restore the state of MIE

Above is only a suggested scheme of operation. Actual software implementation may vary.

## 1.6.4 Registers

For the complete list of interrupt registers and configuration information, please refer to Section 10.4.2 and Section 10.5.2 respectively.
```