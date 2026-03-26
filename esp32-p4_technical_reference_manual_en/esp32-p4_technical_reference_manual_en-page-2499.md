

```markdown
Chapter 47 LP I2S Controller

GoBack

“MI” is an integer value:

$$ MI = \frac{f_{LP\_I2S\_RX\_CLK}}{f_{LP\_I2SI\_BCK\_out} \times MI} $$

$$ f_{LP\_I2SI\_BCK\_out} = \frac{f_{LP\_I2S\_RX\_CLK}}{MI} $$

Note:
LP_I2S_RX_BCK_DIV_NUM must not be configured as 1.

In LP I2S slave mode, make sure $ f_{LP\_I2S\_RX\_CLK} \geq 8 \times f_{BCK} $ to ensure the sampling accuracy. The LP I2S module can output LP_I2S_MCLK_OUT as the master clock for peripherals.

Since in slave mode, the module clock frequency must be greater than or equal to 8 times the BCK clock frequency, the maximum sampling frequency of LP I2S is limited by the data bit width and the number of channels. For example, since the clock source frequency is up to 40 MHz, the module clock can be configured up to 20 MHz, and the BCK clock can be configured up to 5 MHz. Therefore, when transmitting dual-channel 16-bit width data, LP I2S supports sample frequencies up to 78.125 kHz, e.g., 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz. For detailed information, please refer to Section 47.5 RX Clock.

In addition to the clock frequency limitation, LP I2S uses LP I2S internal memory for data storage instead of DMA. Therefore, users need to read data from the LP I2S internal memory in a timely manner. The reading rate may limit the sample frequencies that LP I2S supports. For detailed information, please refer to Section 47.8.3 Internal Memory.

## 47.6 Reset

The units and FIFOs in the LP I2S module are reset by the following bits.

- LP I2S RX units: Reset by the bit `LP_I2S_RX_RESET`;
- LP I2S RX FIFO: Reset by the bits `LP_I2S_RX_FIFO_RESET`.

Note:
The LP I2S module clock must be configured first before the units and FIFO are reset.

## 47.7 Master/Slave RX Mode

The LP I2S supports receiving data either as a master or as a slave in RX mode.

- LP I2S works as a master receiver:

    - Set `LP_I2S_RX_START` to start receiving data. When this bit is set, the RX unit keeps outputting clock signal and sampling input data.
    
    - Configure `LP_I2S_RX_STOP_MODE` to control the suspension of data reception:
        
        * 0: The RX unit only suspends data reception when `LP_I2S_RX_START` is cleared.
        
        * 1: The RX unit suspends data reception when `LP_I2S_RX_START` is cleared or the number of received bytes is greater than the value configured in `LP_I2S_RX_EOF_NUM_REG`. After data
```