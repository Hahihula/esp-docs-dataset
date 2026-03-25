

```markdown
Chapter 31 I2S Controller (I2S) GoBack

In master TX mode, the serial clock BCK for I2S TX unit is I2SO_BCK_out divided from I2S_TX_CLK, which is:

$$f_{\text{I2SO\_BCK\_out}} = \frac{f_{\text{I2S\_TX\_CLK}}}{\text{MO}}$$

“MO” is an integer value:
$$\text{MO} = \text{I2S_TX_BCK_DIV_NUM} + 1$$

Note:
Note that I2S_TX_BCK_DIV_NUM must not be configured as 1.

In master RX mode, the serial clock BCK for I2S RX unit is I2SI_BCK_out divided from I2S_RX_CLK, which is:

$$f_{\text{I2SI\_BCK\_out}} = \frac{f_{\text{I2S\_RX\_CLK}}}{\text{MI}}$$

“MI” is an integer value:
$$\text{MI} = \text{I2S_RX_BCK_DIV_NUM} + 1$$

Note:
* I2S_RX_BCK_DIV_NUM must not be configured as 1.
* In I2S slave mode, make sure $f_{\text{I2S\_TX/RX\_CLK}} >= 8 * f_{\text{BCK}}$. The I2S module can output I2S_MCLK_out as the master clock for peripherals.

31.7 I2S Reset

The units and FIFOs in the I2S module are reset by the following bits.
* I2S TX/RX units: Reset by I2S_TX_RESET and I2S_RX_RESET;
* I2S TX/RX FIFO: Reset by I2S_TX_FIFO_RESET and I2S_RX_FIFO_RESET.

Note:
The I2S module clock must be configured first before the module and FIFO are reset.

31.8 I2S Master/Slave Mode

The ESP32-H2 I2S module can operate as a master or a slave in half-duplex and full-duplex communications, depending on the configuration of I2S_RX_SLAVE_MOD and I2S_TX_SLAVE_MOD.
* I2S_TX_SLAVE_MOD
    - 0: Master TX mode
    - 1: Slave TX mode

Espressif Systems                           904                           ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```