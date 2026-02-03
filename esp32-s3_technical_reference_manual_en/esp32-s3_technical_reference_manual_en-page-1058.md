**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Navigation Link:** GoBack

**Section Titles and Content:**

6. **Enable corresponding interrupts, see Section 28.12.**

7. **Configure DMA outlink.**

8. Set `I2S_TX_STOP_EN` if needed. For more information, please refer to Section [28.8.1](#).

9. Start transmitting data:
   - In master mode, wait till I2Sn slave gets ready, then set `I2S_TX_START` to start transmitting data.
   - In slave mode, set the bit `I2S_TX_START`. When the I2Sn master supplies BCK and WS signals, I2Sn slave starts transmitting data.

10. Wait for the interrupt signals set in Step 6, or check whether the transfer is completed by querying `I2S_TX_IDLE`:
    - O: transmitter is working.
    - 1: transmitter is in idle.

11. Clear `I2S_TX_START` to stop data transfer.

**Subsection Title:** 
28.11.2 Configure I2Sn as RX Mode

**Content of Subsection:**
Follow the steps below to configure I2Sn as RX mode via software:
   1. Configure the clock as described in Section [28.6](#).
   2. Configure signal pins according to Table [28.4-1](#).
   3. Select the mode needed by configuring the bit `I2S_RX_SLAVE_MOD`:
      - O: master RX mode
      - 1: slave RX mode

4. Set needed RX data mode and RX channel mode as described in Section [28.10](#), and then set the bit `I2S_RX_UPDATE`.

5. Reset RX unit and its FIFO according to Section [28.7](#).

6. Enable corresponding interrupts, see Section [28.12](#).

7. Configure DMA inlink, and set the length of RX data in I2S_RXEOF_NUM_REG.

8. Start receiving data:
   - In master mode, when the slave is ready, set `I2S_RX_START` to start receiving data.
   - In slave mode, set `I2S_RX_START` to start receiving data when get BCK and WS signals from the master.

9. The received data is then stored to the specified address of ESP32-S3 memory according to the configuration of DMA. Then the corresponding interrupt set in Step 6 is generated.

**Subsection Title:** 
28.12 I2Sn Interrupts

**Content:**
I2S_TX_HUNG_INT: triggered when transmitting data is timed out. For example, if I2Sn module is configured as TX slave mode, but the master does not provide BCK or WS signal for time specified in.

**Footer Information:** 
Espressif Systems
1058 Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)