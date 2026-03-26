

```markdown
- 1 x state machine (FSM)
- 1 x receiver

The eight channels share a 384 x 32-bit RAM.

## 57.3.2 RAM

### 57.3.2.1 Structure of RAM

Figure 57.3-2 shows the format of pulse code in RAM. Each pulse code contains a 16-bit entry with two fields: "level" and "period". "level" (0 or 1) indicates a low-/high-level value that has been received or is going to be sent, while "period" points out the number of clock cycles (see clk_div in Figure 57.3-1) that the level lasts for.

Figure 57.3-2. Format of Pulse Code in RAM

The minimum value for the period is zero (0) and is interpreted as a transmission end-marker. For a non-zero period (i.e., not an end-marker), its value is limited by APB clock and RMT clock according to the formula below:

$$5 \times T_{apb\_clk} + 6 \times T_{rmt\_sclk} < period \times T_{clk\_div} \quad (57.1)$$

**Note:**

RMT clock and APB clock must satisfy the following relation:

$$1.5 \times T_{apb\_clk} < 9 \times T_{rmt\_sclk} \quad (57.2)$$

According to the formula above and the frequency of rmt_sclk, the pulse width (i.e., period × Tclk_div) able to be captured by RMT is limited as follows:

- The minimum value of pulse width should be larger than (5 × Tapb_clk + 6 × Trmt_sclk).
- The maximum value of pulse width should be smaller than or equal to (the maximum period × the maximum Tclk_div), i.e., ((2^15 − 1) × the maximum Trmt_sclk × 256).

For more information about the rmt_sclk frequency, or APB_CLK frequency, see Section 57.3.3, or Chapter 10 Reset and Clock.
```