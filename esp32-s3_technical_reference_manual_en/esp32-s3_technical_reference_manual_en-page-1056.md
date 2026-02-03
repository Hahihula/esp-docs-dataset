**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**GoBack Link:** [GoBack](#)

---

**Section Heading: Phase Information**

- **Phase II**: The data is read from RX FIFO and converted according to input data mode.

---

**Subsection Title: 28.10.2 Bit Order Control of Channel Data**

The channel data will be stored as the data to be input in order from high to low. The data bit order in each channel is controlled by `I2S_RX_BIT_ORDER`:

- **0**: The bit order of the data to be input is not reversed;
- **1**: The bit order of the data to be input is reversed.

At this point, the first phase of data format control is complete. The data to be input after bit order control is stored in the RX FIFO.

---

**Subsection Title: 28.10.2.2 Bit Width Control of Channel Storage (Valid) Data**

The storage data width in each channel is controlled by `I2S_RX BITS MOD` and `I2S_RX_24 FILL_EN`, see the table below:

| Channel | I2S_RX BITS MOD | I2S_RX_24 FILL_EN |
|---------|-----------------|--------------------|
| Data Width | 31              | x                  |
|          | 23              | 1                  |
|          | 23              | 0                  |
|          | 15              | x                  |
|          | 7               | x                  |

---

**Subsection Title: 28.10.2.3 Bit Width Control of Channel RX Data**

The RX data width in each channel is determined by `I2S_RX TDM_CHAN BITS`:

- If the storage data width in each channel is smaller than the received (RX) data width, then only the bits within the storage data width are saved into memory. Configure `I2S_RX LEFT ALIGN` to:
  - **0**: Only the lower bits of the received data within the storage data width is stored to memory.
  - **1**: Only the higher bits of the received data within the storage data width is stored to memory.

- If the received data width is smaller than the storage data width in each channel, the higher bits of the received data will be filled with zeros and then the data is saved to memory.

---

**Subsection Title: 28.10.2.4 Endian Control Of Channel Storage Data**

The received data is then converted into storage data (to be stored to memory) after some processing, such as discarding extra bits or filling zeros in missing bits. The endian of the storage data is controlled by `I2S_RX BIG ENDIAN` under various data width.

---

**Footer:**
Espressif Systems  
1056  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)