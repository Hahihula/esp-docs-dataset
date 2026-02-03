**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**GoBack Link:** [GoBack](#)

---

### Section with Bullet Points:
- **1**: This channel sends the channel data out.
- **0**: The TX data to be sent by this channel is controlled by `I2S_TX_CHAN_EQUAL`:
  - **1**: The data of previous channel is sent out.
  - **0**: The data stored in `I2S_SINGLE_DATA` is sent out.

### Section with Description and Variables (In TDM master mode, WS signal control):
- In TDM master mode, WS signal controlled by `I2S_TX_WS_IDLE_POL` and `I2S_TX_TDM_WS_WIDTH`:
  - `I2S_TX_WS_IDLE_POR`: the default level of WS signal
  - `I2S_TX_TDM_WS_WIDTH`: the cycles the WS default level lasts for when transmitting all channel data

### Section with Description (TDM Channel Configuration Example):
- In this example, the register configuration is as follows:
  - `I2S_TX_TDMTot_CHANNUM = 5`, i.e., channel 0 ~ 5 are used to transmit data
  - `I2S_TX_CHAN_EQUAL = 1`, i.e., that data of previous channel will be transmitted if the bit in `I2S_TX_TDM_CHANn_EN` is cleared. \( n = 0 \sim 5 \)
  - `I2S_TX_TDM_CHAN0/2/5_EN = 1`, i.e., these channels send their channel data out.
  - `I2S_TX_TDM_CHAN1/3/4_EN = 0`, i.e., these channels send the previous channel data out.

### Section with Description (Once configuration is done, data transmission):
- Once the configuration is done, data transmitted as follows:

**Figure Caption:**
Figure 28.9-2. TDM Channel Control

**Diagram Description in Text Format:**  
```
Channel 0   Channel 1   Channel 2   Channel 3   Channel 4   Channel 5
Data_0     Data_0      Data_2       Data_2       Data_2       Data_5
I2S_TX_TDM_CHAN0_EN = 1; I2S_TX_CHAN_EQUAL = 1;
I2S_TX_TDM_CHAN1_EN = 0; I2S_TX_CHAN2_EN = 1;
I2S_TX_TDM_CHAN3_EN = 0; I2S_TX_CHAN4_EN = 0; I2S_TX_CHAN5_EN = 1;
```

### Subsection Title:**
28.9.2.2 I2Sn Channel Control in PDM Mode

**Subsection Description with Variables (In PDM mode, fetching data from DMA control):**
- In PDM mode, fetching data from DMA is controlled by `I2S_TX_MONO` and `I2S_TX_MONO_FST_VLD`, see the table below. Please configure these two bits according to the data stored in memory, be it single-channel or dual-channel data.

**Footer:**
Espressif Systems  
1051  
ESP32-S3 TRM (Version 1.7)  

**Links at Footer:**  
Submit Documentation Feedback