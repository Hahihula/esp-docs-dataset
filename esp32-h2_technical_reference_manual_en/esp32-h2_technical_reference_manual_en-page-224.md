

```markdown
## 6.5.3 Simple GPIO Output

GPIO matrix can also be used for simple GPIO output. For this case, one GPIO pin can be configured to directly output the desired value, without routing any peripheral output to this pin. This can be done as below:

* Set GPIO matrix `GPIO_FUNC_OUT_SEL` with a special peripheral index 128 (0x80);
* Set the corresponding bit in `GPIO_OUT_REG` register to the desired GPIO output value.

**Note:**
* `GPIO_OUT_REG[0] ~ GPIO_OUT_REG[27]` correspond to `GPIO0 ~ GPIO27` respectively. `GPIO_OUT_REG[28] ~ GPIO_OUT_REG[31]` are invalid.
* Recommended operation: use `GPIO_OUT_WTS/GPIO_OUT_W1TC` to set or clear the register `GPIO_OUT_REG`.

## 6.5.4 Sigma Delta Modulated Output (SDM)

### 6.5.4.1 Functional Description

Four out of the 99 peripheral output signals (index: 83 ~ 86 in Table 6.12-1 support 1-bit second-order sigma delta modulation. By default the output is enabled for these four channels. This Sigma Delta modulator can also output PDM (pulse density modulation) signal with configurable duty cycle. The transfer function is:

$$H(z) = X(z)z^{-1} + E(z)(1-z^{-1})^2$$

E(z) is quantization error and X(z) is the input.

This modulator supports scaling down of IO MUX operating clock by divider 1 ~ 256:

* Set `GPIO_EXT_FUNCTION_CLK_EN` to enable the modulator clock.
* Configure `GPIO_EXT_SDn_PRESCALE (n = 0 ~ 3 for the four channels)`.

After scaling, the clock cycle is equal to one pulse output cycle from the modulator.

`GPIO_EXT_SDn_IN` is a signed number with a range of [-128, 127] and is used to control the duty cycle¹ of PDM output signal.

* `GPIO_EXT_SDn_IN = -128`, the duty cycle of the output signal is 0%.
* `GPIO_EXT_SDn_IN = 0`, the duty cycle of the output signal is near 50%.
* `GPIO_EXT_SDn_IN = 127`, the duty cycle of the output signal is near 100%.

The formula for calculating PDM signal duty cycle is shown as below:

$$Duty\_Cycle = \frac{GPIO\_EXT\_SDn\_IN + 128}{256}$$

**Note:**
For PDM signals, duty cycle refers to the percentage of high level cycles to the whole statistical period (several pulse cycles, for example, 256 pulse cycles).
```