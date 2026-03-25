

```markdown
- O: The channel data is invalid and will not be stored into RX FIFO.

In TDM master mode, WS signal is controlled by I2S_RX_WS_IDLE_POL and I2S_RX_TDM_WS_WIDTH.
* I2S_RX_WS_IDLE_POL: The default level of WS signal;
* I2S_RX_TDM_WS_WIDTH: The cycles the WS default level lasts for when receiving all channel data.

I2S_RX_HALF_SAMPLE_BITS x 2 is equal to the BCK cycles in one WS period.


### 31.10.1.2 PDM RX Mode

In PDM RX mode, I2S supports PDM raw data reception. It converts the serial data from channels to the data to be entered into memory.

In PDM RX master mode, the default level of the WS signal is controlled by I2S_RX_WS_IDLE_POL. WS frequency is half of the BCK frequency. The configuration of the BCK signal is similar to that of WS signal as described in Section 31.6. Note, in PDM RX mode, the value of I2S_RX_HALF_SAMPLE_BITS must be same as that of I2S_RX_BITS_MOD.


### 31.10.2 Data Format Control

The data format is controlled in the following phases:
* Phase I: Serial input data is converted into the data to be saved to RX FIFO;
* Phase II: The data is read from RX FIFO and converted according to the input data mode.

#### 31.10.2.1 Bit Order Control of Channel Data

The channel data will be stored as the data to be input in order from high to low. The data bit order in each channel is controlled by I2S_RX_BIT_ORDER:
* O: The bit order of the data to be input is not reversed;
* 1: The bit order of the data to be input is reversed.

At this point, the first phase of data format control is completed. The data to be input after bit order control is stored in the RX FIFO.


#### 31.10.2.2 Bit Width Control of Channel Storage (Valid) Data

The storage data width in each channel is controlled by I2S_RX_BITS_MOD and I2S_RX_24_FILL_EN. See the table below.

Table 31.10-1. Channel Storage Data Width
| Channel Storage Data Width | I2S_RX_BITS_MOD | I2S_RX_24_FILL_EN |
|----------------------------|------------------|-------------------|
| 32                         | 31               | x                 |
|                            | 23               | 1                 |
| 24                         | 23               | 0                 |
| 16                         | 15               | x                 |
| 8                          | 7                | x                 |
```