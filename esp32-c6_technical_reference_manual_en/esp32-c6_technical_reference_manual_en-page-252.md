

```markdown
$$H(z) = X(z)z^{-1} + E(z)(1-z)^{-1}$$

E(z) is quantization error and X(z) is the input.

This modulator supports scaling down of IO MUX operating clock by divider 1 ~ 256:

* Set `GPIO_EXT_SD_FUNCTION_CLK_EN` to enable the modulator clock.
* Configure `GPIO_EXT_SDn_PRESCALE` (n = 0 ~ 3 for the four channels).

After scaling, the clock cycle is equal to one pulse output cycle from the modulator.

`GPIO_EXT_SDn_IN` is a signed number with a range of [-128, 127] and is used to control the duty cycle¹ of PDM output signal.

* `GPIO_EXT_SDn_IN = -128`, the duty cycle of the output signal is 0%.
* `GPIO_EXT_SDn_IN = 0`, the duty cycle of the output signal is near 50%.
* `GPIO_EXT_SDn_IN = 127`, the duty cycle of the output signal is near 100%.

The formula for calculating PDM signal duty cycle is shown as below:

$$Duty\_Cycle = \frac{GPIO\_EXT\_SDn\_IN + 128}{256}$$

**Note:**
For PDM signals, duty cycle refers to the percentage of high level cycles to the whole statistical period (several pulse cycles, for example, 256 pulse cycles).

### 7.5.4.2 SDM Configuration

The configuration of SDM is shown below:

* Route one of SDM outputs to a pin via GPIO matrix, see Section 7.5.2.
* Enable the modulator clock by setting `GPIO_EXT_SD_FUNCTION_CLK_EN`.
* Configure the divider value by setting `GPIO_EXT_SDn_PRESCALE`.
* Configure the duty cycle of SDM output signal by setting `GPIO_EXT_SDn_IN`.

## 7.6 Direct Input and Output via IO MUX

### 7.6.1 Overview

Some digital signals (SPI and JTAG) can bypass GPIO matrix for better high-frequency digital performance. In this case, IO MUX is used to connect these pins directly to peripherals.

This option is less flexible than routing signals via GPIO matrix, as the IO MUX register for each GPIO pin can only select from a limited number of functions, but high-frequency digital performance can be improved.
```