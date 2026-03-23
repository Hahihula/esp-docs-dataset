

```markdown
- GPIO_FUNCn_OEN_SEL = 0: use the output enable signal from peripheral, for example SPIQ_oe in the column "Output enable signal when GPIO_FUNCn_OEN_SEL = 0" of Table 7.11-1. Note that the signals such as SPIQ_oe can be 1 (1'd1) or 0 (1'd0), depending on the configuration of corresponding peripherals. If it's 1'd1 in column "Output enable signal when GPIO_FUNCn_OEN_SEL = 0", it indicates that once GPIO_FUNCn_OEN_SEL is cleared, the output signal is always enabled by default.

Note:
Signals are numbered consecutively, but not all signals are valid.
- Only the signals with a name assigned in the column "Input signal" in Table 7.11-1 are valid input signals.
- Only the signals with a name assigned in the column "Output signal" in Table 7.11-1 are valid output signals.
```