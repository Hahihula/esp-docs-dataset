**Title: Chapter 22 I2S Controller (I2S)**

---

### Figure Caption:
- **Figure 22.4-1. Tx FIFO Data Mode**

| Tx data | Dₙ₋₁ | Dₙ |
|---------|------|----|
| Tx Address | addr₀ | addr₁ |
| Tx FIFO mode0 | Data | Dₙ₋₁ |
| Tx FIFO Address | addr₀ | addr₁ | addr₂ | addr₃ |
| Tx FIFO mode1 | Data | D'ₙ₋₁ | D''ₙ₋₁ | D'n | D'' |

---

### Table Caption:
- **Table 22.4-1. Register Configuration**

| I2S_TX_FIFO_MODE[2:0] | Description |
|------------------------|-------------|
| Tx FIFO mode0          | 0           | 16-bit dual channel data |
| Tx FIFO mode1          | 2           | 32-bit single channel data |
| Tx FIFO mode1          | 3           | 32-bit single channel data |
| Tx FIFO mode1          | 1           | 16-bit single channel data |

---

### Body Text:
At the first stage, there are two modes for data to be sent and written into FIFO. In Tx FIFO mode0, the Tx data-to-be-sent are written into FIFO according to the time order. In Tx FIFO mode1, the data-to-be-sent are divided into 16 high- and 16 low-order bits. Then both the 16 high- and 16 low-order bits are recomposed and written into FIFO. The details are shown in Figure 22.4-4 with the corresponding registers listed in Table 22.4-1.

D'ₙ consists of 16 high-order bits of Dₙ, and it is followed by zeros (0). D''ₙ consists of 16 low-order bits of Dₙ, also preceded by zero bits to make a total length as shown in Figure 22.4-4.

At the second stage, the system reads data that will be sent from FIFO according to the relevant register configuration. The mode in which the system reads data from FIFO is irrelevant for I2S_TX_FIFO_MOD[2:0] and I2S_TX_CHAN_MOD[2:0]. I2S_TX_FIFO_MOD[2:0] determines whether the data are 16-bit or 32-bit, as shown in Table 22.4-1, while I2S_TX_CHAN_MOD[2:0] determines the format of the data-to-be-sent, as shown in Table 22.4-2.

---

### Table Caption:
- **Table 22.4-2. Send Channel Mode**

| Description | |
|-------------|----|
| Dual channel mode | |
| Mono mode    | When I2S_TX_MS Right equals O, the left-channel data are "holding" their values and the right-channel data change into the left-channel data. |
|               | When I2S_TX_MS RIGHT equals 1, the right-channel data are "holding" their values and the left-channel data change into the right-channel data. |

---

### Footer:
- **Espressif Systems**
- Page number: 421
- Document version: ESP32 TRM (Version 5.6)
- Link to submit documentation feedback

---