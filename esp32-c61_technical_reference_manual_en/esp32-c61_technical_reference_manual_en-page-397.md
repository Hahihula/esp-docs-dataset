

```markdown
## 9.5.4 Delegated Interrupts

The ESP32-C61 RISC-V CPU supports Machine Mode and User Mode. The 32 external HP CPU interrupts can be configured as either Machine Mode interrupts or User Mode interrupts. When the HP CPU is in Machine Mode, it only responds to Machine Mode interrupts and does not respond to User Mode interrupts. When the HP CPU is in User Mode, it can respond to all interrupts.

Under normal conditions, User Mode interrupts are only handled when the CPU is operating in User Mode. However, with the interrupt delegation feature, Machine Mode can be configured to handle certain User Mode interrupts, while the CPU itself remains in Machine Mode. This is achieved by configuring registers to delegate User Mode interrupts to Machine Mode interrupts.

- Each interrupt source of the interrupt matrix can independently enable or disable the interrupt delegation feature.
- Multiple interrupt sources from the interrupt matrix can enable the interrupt delegation feature at the same time.
- Delegation is allowed to only one interrupt signal from the interrupt matrix.

Software can configure the `INTMTX_COREO_INT_SIG_IDX_ASSERT_IN_SEC_REG` register to n to delegate a User Mode interrupt to a Machine Mode interrupt with interrupt number n.

To enable the delegated interrupt function for interrupt source SOURCE in the interrupt matrix, software can set the corresponding bit in the `INTMTX_COREO_SOURCE_INTR_PASS_IN_SEC_REG` register to 1.

## 9.5.5 Query Current Interrupt Status of SOURCE

After enabling a SOURCE, you can query its current interrupt status by reading the corresponding bit value in `INTMTX_COREO_INT_STATUS_n_REG` (read only). For the mapping between `INTMTX_COREO_INT_STATUS_n_REG` and the SOURCE, please refer to Table 9.5-1.
```