

```markdown
- 0: The bit order of the data to be input is not reversed;
- 1: The bit order of the data to be input is reversed.

At this point, the first phase of data format control is completed.

## 47.8.2.2 Bit Width Control of Channel RX Data

The storage data width in each channel is controlled by `LP_I2S_RX_BITS_MOD`. For ESP32-P4 LP I2S, the value of `LP_I2S_RX_BITS_MOD` is fixed as 15. The corresponding channel storage data width is 16 bit.

## 47.8.2.3 Bit Width Control of Channel RX Data

The RX data width in each channel is determined by `LP_I2S_RX_TDM_CHAN_BITS`.

- If the storage data width in each channel is smaller than the received (RX) data width, then only the bits within the storage data width is saved into memory. Configure `LP_I2S_RX_LEFT_ALIGN` to:
  - 0: Only the lower bits of the received data within the storage data width is stored to memory;
  - 1: Only the higher bits of the received data within the storage data width is stored to memory.
- If the received data width is smaller than the storage data width in each channel, the higher bits of the received data will be filled with zeros and then the data is saved to memory.

## 47.8.2.4 Endian Control of Channel Storage Data

The received data is then converted into storage data (to be stored to memory) after some processing, such as discarding extra bits or filling zeros in missing bits. The endian of the storage data is controlled by `LP_I2S_RX_BIG_ENDIAN` (the data bit width is fixed as 16). See the table below.

Table 47.8-2. Channel Storage Data Endian

| Original Data | Endian of Processed Data | LP_I2S_RX_BIG_ENDIAN |
|---------------|--------------------------|----------------------|
| {B1, B0}      | {B1, B0}                 | 0                    |
|               | {B0, B1}                 | 1                    |

At this point, the data format control is completed. Data then is stored into memory.

## 47.8.3 Internal Memory

All data after format control is stored in the LP I2S internal memory, which is a 16-bit wide circular buffer that supports RX unit write operations and system read operations. The LP I2S internal memory includes a pair of hardware-maintained read and write pointers to manage write and read operations.

1. When LP I2S writes data:
   - If the memory is full: Overwrites the oldest data and increments the write and read pointers by 1 (the value of the read pointer is the value of the write pointer plus one at this point).
   - If the memory is not full: Writes the data and increments the write pointer by 1. The read pointer remains unchanged.

2. When the system reads from the LP I2S memory:
```