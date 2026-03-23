

```markdown
channel O ~ 5 will be used to receive data.

In these RX channels, if I2S_RX_TDM_CHANn_EN is set to:

*   1: this channel data is valid and will be stored into RX FIFO;
*   0: this channel data is invalid and will not be stored into RX FIFO.

In TDM master mode, WS signal is controlled by I2S_RX_WS_IDLE_POL and I2S_RX_TDM_WS_WIDTH.
*   I2S_RX_WS_IDLE_POL: the default level of WS signal;
*   I2S_RX_TDM_WS_WIDTH: the cycles the WS default level lasts for when receiving all channel data.

I2S_RX_HALF_SAMPLE_BITS × 2 is equal to the BCK cycles in one WS period.


### 30.10.1.2 I2S Channel Control in PDM RX Mode

In PDM RX mode, I2S converts the serial data from channels to the data to be entered into memory.

In PDM RX master mode, the default level of WS signal is controlled by I2S_RX_WS_IDLE_POL. WS frequency is half of BCK frequency. The configuration of BCK signal is similar to that of WS signal as described in Section 30.6. Note, in PDM RX mode, the value of I2S_RX_HALF_SAMPLE_BITS must be same as that of I2S_RX_BITS_MOD.


### 30.10.2 Data Format Control

Data format is controlled in the following phases:

*   Phase I: serial input data is converted into the data to be saved to RX FIFO;
*   Phase II: the data is read from RX FIFO and converted according to the input data mode.

#### 30.10.2.1 Bit Order Control of Channel Data

The channel data will be stored as the data to be input in order from high to low. The data bit order in each channel is controlled by I2S_RX_BIT_ORDER:

*   0: The bit order of the data to be input is not reversed;
*   1: The bit order of the data to be input is reversed.

At this point, the first phase of data format control is completed.


#### 30.10.2.2 Bit Width Control of Channel Storage (Valid) Data

The storage data width in each channel is controlled by I2S_RX_BITS_MOD and I2S_RX_24_FILL_EN. See the table below.
```