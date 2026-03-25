

```markdown
To configure the integer divider, clear `PCR_I2S_TX/RX_CLKM_DIV_X` and `PCR_I2S_TX/RX_CLKM_DIV_Z`, then set `PCR_I2S_TX/RX_CLKM_DIV_Y` to 1.

**Note:**
Using fractional divider may introduce some clock jitter.

In master TX mode, the serial clock BCK for I2S TX unit is I2SO_BCK_out divided from I2S_TX_CLK which is:

$$f_{I2SO\_BCK\_out} = \frac{f_{I2S\_TX\_CLK}}{MO}$$

“MO” is an integer value:

$$MO = I2S\_TX\_BCK\_DIV\_NUM + 1$$

**Note:**
Note that `I2S_TX_BCK_DIV_NUM` must not be configured as 1.

In master RX mode, the serial clock BCK for I2S RX unit is I2SI_BCK_out divided from I2S_RX_CLK, which is:

$$f_{I2SI\_BCK\_out} = \frac{f_{I2S\_RX\_CLK}}{MI}$$

“MI” is an integer value:

$$MI = I2S\_RX\_BCK\_DIV\_NUM + 1$$

**Note:**
* `I2S_RX_BCK_DIV_NUM` must not be configured as 1.
* In I2S slave mode, make sure $f_{I2S\_TX/RX\_CLK} \geq 8 * f_{BCK}$. The I2S module can output `I2S_MCLK_out` as the master clock for peripherals.

## 35.7 I2S Reset

The units and FIFOs in the I2S module are reset by the following bits.
* I2S TX/RX units: Reset by `I2S_TX_RESET` and `I2S_RX_RESET`;
* I2S TX/RX FIFO: Reset by `I2S_TX_FIFO_RESET` and `I2S_RX_FIFO_RESET`.

**Note:**
The I2S module clock must be configured first before the module and FIFO are reset.
```