**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Section Header:**
Register 37.5 RMT_CHmCONF1_REG (m = 4, 5, 6, 7) (0x003C, 0x004C, 0x0044, 0x004C)

**Hexadecimal Address Table:**
- Offset | Name
- ------ | ------
- 16     | RMT_CONF_UPDATE_Chm
- 15     | (reserved)
- 14     | RMT_MEM_RX_WRAP_EN_CHm
- 13     | (reserved)
- 12     | RMT_RX_FILTER_THRES_CHm
- 5      | Reset
- 0      | Oxf

**Field Descriptions:**
- **RMT_RX_EN_CHm**: Set this bit to enable the receiver to start receiving data on channel m. (R/W)
- **RMT_MEM_WR_RST_CHm**: Set this bit to reset RAM write address accessed by the receiver for channel m. (WT)
- **RMT_ABP_MEM_RST_CHm**: Set this bit to reset RAM W/R address accessed by APB FIFO for channel m. (WT)
- **RMT_MEM_OWNER_CHm**: This bit marks the ownership of channel m’s RAM block. (R/W/SC)

**Descriptions:**
1'h1': Receiver is using the RAM.
1'h0': APB bus is using the RAM.

- Set this bit to enable the receiver's filter for channel m. (R/W)
- When receiving data, the receiver ignores the input pulse when its width is shorter than this register value in units of rmt_sclk cycles. (R/W)

**Additional Fields:**
- **RMT_MEM_RX.WRAP_EN_CHm**: Set this bit to enable wrap RX mode for channel m. In this mode, if the RX data size is larger than channel m’s RAM block size, the receiver stores the RX data from the first address to the last address in loops. (R/W)
- Synchronization bit for channel m. (WT)

**Footer:**
Espressif Systems
1430 ESP32-S3 TRM (Version 1.7)