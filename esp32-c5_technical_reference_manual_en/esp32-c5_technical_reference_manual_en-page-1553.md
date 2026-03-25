

```markdown
PWMxA Input
            ┌───────────────┐
            │               │
            │    ┌────────┐ │
            │    │       │ │
            │    │  ┌─────┼─► DTFED
            │    │  │     │
            │    │  │     │
            │    │  │     │
            │    │  │     │
            │    │  │     │
            │    │  │     │
            │    └────────┘
            │               │
PWMxA Output ──────────────┼───────────────────────────────────────────
PWMxB Output ──────────────┴───────────────────────────────────────────

Figure 41.3-25. Active Low (AL) Dead Time Waveforms
```

RED and FED delays may be set up independently. The delay value is programmed using the 16-bit field `MCPWM_DBn_RED` and `MCPWM_DBn_FED`. The register value represents the number of clock (`DT_clk`) periods by which a signal edge is delayed. `DT_clk` can be selected from `PWM_clk` or `PT_clk` through register `MCPWM_DBn_CLK_SEL`.

To calculate the delay on the falling edge (FED) and rising edge (RED), use the following formulas:

```latex
FED = MCPWM_DTn_FED \times T_{DT\_clk}
```

```latex
RED = MCPWM_DTn_RED \times T_{DT\_clk}
```