**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Section Titles and Content:**

1. **22.4.6 I2S Master/Slave Mode**
   - The ESP32 I2S module can be configured to act as a master or slave device on the I2S bus.
   - It supports slave transmitter and receiver configurations in addition to master transmitter and receiver configurations, supporting full-duplex and half-duplex communication over the I2S bus.

   **Subsection:**
   - `I2S_RX_SLAVE_MOD` bit of register `I2S_CONF_REG` can configure I2S to slave receiving mode.
   - `I2S_TX_SLAVE_MOD` bit is used for configuring master transmitting and slave receiving modes, respectively. When in master transmitting mode (`I2S_TX_START` set), the module will keep driving clock signal on left and right channels until FIFO sends out all buffered data or there are no new data to shift; last batch of data loops back.
   - When `I2S_RX_START` bit is reset, it stops I2S from transmitting mode. The master waits for BCK clock enable a transmit operation.

   **Subsection:**
   - `I2S_RX_START` in slave receiving mode keeps driving the input signal and sampling data until this bit resets.
   - When set to receive operations (`I2S_CONF_REG`), it enables I2S module waiting on master BCK for enabling reception. 

2. **22.4.7 I2S PDM**
   - ESP32 allows pulse density modulation (PDM) conversion between PCM and PDM signals.
   - The output clock of the PDM is mapped to `I2S0*_WS_out` signal, identical configuration as BCK.

   **Table: 22.4-5 lists configurations for I2S_TX_PDM_BIT and I2S_TX_PDM_FS bit**
   - Table details are not provided in text but referenced with Figure caption.
   
3. **Figure Caption (22.4-7): PDM Transmitting Module**

   The diagram shows:
   - PCM signal is filtered through a high-pass filter (`HPF`).
   - Filtered signals pass to an LPF and then combined into `PDM` group0.

   Formula for frequency relation: 
   \[
   f_{\text{pdm}} = 64 \times f_{\text{pcm}}
   \]
   Where:
   - \(f_{\text{pdm}}\) is the PDM signal's frequency.
   - \(f_{\text{PCM}}\) is the PCM signal’s frequency.

**Footer:**
- Table reference for I2S_PDM configuration rates
- Page number 424, ESP32 TRM (Version 5.6)
- Submit Documentation Feedback link

**Navigation Links and Buttons:** 
- GoBack button at top right corner.
- Submit Documentation Feedback text in footer.

(Note: The exact content of the table is not provided but referenced with a figure caption.)