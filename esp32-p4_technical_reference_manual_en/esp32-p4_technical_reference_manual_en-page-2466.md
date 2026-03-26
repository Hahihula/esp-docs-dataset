

```markdown
| Input Data Signal | Channel          | Enable Register                                      |
|-------------------|------------------|------------------------------------------------------|
| I2SO1_Data_in     | Left channel     | I2S_RX_TDM_PDM_CHANO_EN                             |
|                   | Right channel    | I2S_RX_TDM_PDM_CHAN1_EN                             |
| I2SO1_Data_in     | Left channel     | I2S_RX_TDM_PDM_CHAN2_EN                             |
|                   | Right channel    | I2S_RX_TDM_PDM_CHAN3_EN                             |
| I2SO2_Data_in     | Left channel     | I2S_RX_TDM_PDM_CHAN4_EN                             |
|                   | Right channel    | I2S_RX_TDM_PDM_CHAN5_EN                             |
| I2SO3_Data_in     | Left channel     | I2S_RX_TDM_PDM_CHAN6_EN                             |
|                   | Right channel    | I2S_RX_TDM_PDM_CHAN7_EN                             |

## 46.10.2 Data Format Control

The data format of I2Sn is controlled in the following phases:

* Phase I: Serial input data is converted into the data to be saved to RX FIFO;
* Phase II: The data is read from RX FIFO and converted according to the input data mode.

### 46.10.2.1 Bit Order Control of Channel Data

The channel data will be stored as the data to be input in order from high to low. The data bit order in each channel is controlled by I2S_RX_BIT_ORDER:

* 0: The bit order of the data to be input is not reversed;
* 1: The bit order of the data to be input is reversed.
```