

```markdown
## 5.5.3 Simple GPIO Output

GPIO matrix can also be used for simple GPIO output. This can be done as below:

- Set GPIO matrix `GPIO_FUNCn_OUT_SEL` with a special peripheral index 128 (0x80);
- Set the corresponding bit in `GPIO_OUT_REG` register to the desired GPIO output value.

**Note:**

- `GPIO_OUT_REG[0] ~ GPIO_OUT_REG[21]` correspond to GPIO0 ~ GPIO21, and `GPIO_OUT_REG[25:22]` are invalid.
- Recommended operation: use corresponding W1TS and W1TC registers, such as `GPIO_OUT_W1TS/GPIO_OUT_W1TC` to set or clear the registers `GPIO_OUT_REG`.

## 5.5.4 Sigma Delta Modulated Output (SDM)

### 5.5.4.1 Functional Description

Four out of the 125 peripheral outputs (output index: 55 ~ 58 in Table 5.11-1) support 1-bit second-order sigma delta modulation. By default output is enabled for these four channels. This modulator can also output PDM (pulse density modulation) signal with configurable duty cycle. The transfer function of this second-order SDM modulator is:

$$H(z) = X(z)z^{-1} + E(z)(1 - z^{-1})^2$$

E(z) is quantization error and X(z) is the input.

Sigma Delta modulator supports scaling down of APB_CLK by divider 1 ~ 256:

- Set `GPIO SD FUNCTION CLK_EN` to enable the modulator clock.
- Configure register `GPIO SDn_PRESCALE` (n is 0 ~ 3 for four channels).

After scaling, the clock cycle is equal to one pulse output cycle from the modulator.

`GPIO SDn_IN` is a signed number with a range of [-128, 127] and is used to control the duty cycle¹ of PDM output signal.

- `GPIO SDn_IN = -128`, the duty cycle of the output signal is 0%.
- `GPIO SDn_IN = 0`, the duty cycle of the output signal is near 50%.
- `GPIO SDn_IN = 127`, the duty cycle of the output signal is close to 100%.

The formula for calculating PDM signal duty cycle is shown as below:

$$Duty\_Cycle = \frac{GPIO SDn_IN + 128}{256}$$

**Note:**

For PDM signals, duty cycle refers to the percentage of high level cycles to the whole statistical period (several pulse cycles, for example 256 pulse cycles).
```