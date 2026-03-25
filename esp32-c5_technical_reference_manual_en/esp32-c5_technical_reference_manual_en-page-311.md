

```markdown
LP GPIO matrix supports only the Simple GPIO Output function. There is no need to configure function selection registers. Just configure the corresponding bit in LP_GPIO_OUT_REG to the desired GPIO output value.

Note:
- The bits LP_GPIO_OUT_REG[0~6] correspond to GPIO0~GPIO6.
- Recommended operation: use LP_GPIO_OUT_DATA_W1TS and LP_GPIO_OUT_DATA_W1TC to set or clear LP_GPIO_OUT_REG.
```

## 8.5.3 Sigma Delta Modulated Output (SDM)

### 8.5.3.1 Functional Description

Four HP peripheral output signals (index: 76~79 in Table 8.12-1) support 1-bit second-order sigma delta modulation. By default the output is enabled for these four channels. This Sigma Delta modulator can also output PDM (pulse density modulation) signal with configurable duty cycle. The function is:

$$H(z) = X(z)z^{-1} + E(z)(1-z^{-1})^2$$

E(z) is quantization error and X(z) is the input.

This modulator supports scaling down of IO MUX operating clock by divider 1~256:

- Set GPIO_EXT_SIGMADELTA_CLK_EN to enable the modulator clock.
- Configure GPIO_EXT_SDn_PRESCALE (n = 0~3 for the four channels).

After scaling, the clock cycle is equal to one pulse output cycle from the modulator.

GPIO_EXT_SDn_IN is a signed number with a range of [-128, 127] and is used to control the duty cycle¹ of PDM output signal.

- GPIO_EXT_SDn_IN = -128, the duty cycle of the output signal is 0%.
- GPIO_EXT_SDn_IN = 0, the duty cycle of the output signal is near 50%.
- GPIO_EXT_SDn_IN = 127, the duty cycle of the output signal is near 100%.

The formula for calculating PDM signal duty cycle is shown as below:

$$Duty\_Cycle = \frac{GPIO\_EXT\_SDn\_IN + 128}{256}$$

Note:
For PDM signals, duty cycle refers to the percentage of high level cycles to the whole statistical period (several pulse cycles, for example, 256 pulse cycles).

### 8.5.3.2 SDM Configuration

The configuration of SDM is shown below:
```