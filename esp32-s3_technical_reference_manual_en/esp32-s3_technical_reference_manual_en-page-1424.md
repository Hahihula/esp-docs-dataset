**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Section Header:**
37.5 Register Summary

**Body Text:**
The addresses in this section are relative to RMT base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers (Column Titles):**
- Name
- Description
- Address
- Access

**Table Content:**

1. **FIFO R/W Register**
   - **RMT_CHODATA_REG**: The read and write data register for channel 0 by APB FIFO access, Address: `0x0000`, Access: RO.
   - **RMT_CH1DATA_REG**: The read and write data register for channel 1 by APB FIFO access, Address: `0x0004`, Access: RO.
   - **RMT_CH2DATA_REG**: The read and write data register for channel 2 by APB FIFO access, Address: `0x0008`, Access: RO.
   - **RMT_CH3DATA_REG**: The read and write data register for channel 3 by APB FIFO access, Address: `0x000C`, Access: RO.
   - **RMT_CH4DATA_REG**: The read and write data register for channel 4 by APB FIFO access, Address: `0x0010`, Access: RO.

2. **Configuration Registers**
   - **RMT_CHOCONFO_REG**: Configuration register O for channel 0, Address: `0x0020`, Access varies.
   - **RMT_CH1CONFO_REG**: Configuration register O for channel 1, Address: `0x0024`, Access varies.
   - **RMT_CH2CONFO_REG**: Configuration register O for channel 2, Address: `0x0028`, Access varies.
   - **RMT_CH3CONFO_REG**: Configuration register O for channel 3, Address: `0x002C`, Access varies.
   - **RMT_CH4CONFO_REG**: Configuration register O for channel 4 (read/write), Address: `0x0030`, Access R/W.

3. **Configuration Registers Continued**
   - **RMT_CH4CONF1_REG**: Configuration register 1 for channel 4, Address: `0x0034`, Access varies.
   - **RMT_CH5CONFO_REG**: Configuration register O for channel 5 (read/write), Address: `0x0038`, Access R/W.

4. **Configuration Registers Continued**
   - **RMT_CH6CONFO_REG**: Configuration register 1 for channel 6, Address: `0x0040`, Access varies.
   - **RMT_CH7CONFO_REG**: Configuration register O for channel 7 (read/write), Address: `0x0048`, Access R/W.

5. **Configuration Registers Continued**
   - **RMT_CH7CONF1_REG**: Configuration register 1 for channel 7, Address: `0x004C`, Access varies.
   - **RMT_CH4_RX_CARRIER_RMPEG**: Demodulation register for channel 4 (read/write), Address: `0x0090`, Access R/W.

6. **Configuration Registers Continued**
   - **RMT_CH5_RX_CARRIER_RMPEG**: Demodulation register for channel 5, Address: `0x0094`, Access varies.
   - **RMT_CH6_RX_CARRIER_RMPEG**: Demodulation register for channel 6 (read/write), Address: `0x0098`, Access R/W.

7. **Configuration Registers Continued**
   - **RMT_CH7_RX_CARRIER_RMPEG**: Demodulation register for channel 7, Address: `0x009C`, Access varies.
   - **RMT_SYS_CONF_REG**: Configuration register for RMT APB (read/write), Address: `0x00C0`, Access RO.

8. **Status Registers**
   - **RMT_REF_CNT_RST_REG**: Reset register for RMT clock divider, Address: `0x00C8`, Access WT

**Footer Information:**
Espressif Systems
1424 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback