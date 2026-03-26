

```markdown
- 512 x 32-bit words
- 1024 x 16-bit words
- 2048 x 8-bit words

The LUT RAM can be used to do translations of data, e.g. using a calibration curve for a given sensor. It can also be used to implement mathematical functions, with the address input split into two or more input variables and the data output used as the output of the function; the memory should be loaded with the output of the function for each of the input values.

*   32 bits from 2 x 16-bit counters (i.e., CTR A/B block in Figure 59.3-1). This register contains two 16-bit counters, named 'A' and 'B'. These can be loaded, incremented and decremented via control path instructions.
*   30 bits from comparators between counter B and the previous data on the output (PREV OUT in Figure 59.3-1; the 30 bits described here are part of the AUX block there). These allow the result of comparisons being used for output or for program flow. This can be useful in e.g. decoding run-length encoded streams, or generating PWM signals.
*   2 bits, one fixed-high, one fixed-low (i.e., part of AUX in Figure 59.3-1). These are useful if a protocol needs an always-high or always-low bit in the output that does not depend on the input data.

Note that some sources cannot be accessed at the same time. Specifically, a given instruction cannot source data from both the high 32 bits of the input FIFO source register as well as the counter registers. When data is read from the LUT, for a LUT that is set to a width of N, the top N bits of both the input FIFO register as well as the top N bits of the counter register become unavailable.

### 59.3.2 Control Path

Figure 59.3-2. BitScrambler Control Path Diagram
```