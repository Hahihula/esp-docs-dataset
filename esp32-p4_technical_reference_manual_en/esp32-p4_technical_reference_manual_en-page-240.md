

```markdown
Based on the assumptions at the beginning of this section, the calculation matrix would be 5 rows and 13 columns, and the actual hardware CRC calculation formulas would be as follows (⊕represents the XOR operation):

crc[0] = crc_tmp[0] ⊕ crc_tmp[2] ⊕ crc_tmp[3] ⊕ data[0] ⊕ data[3] ⊕ data[5] ⊕ data[6]
crc[1] = crc_tmp[1] ⊕ crc_tmp[3] ⊕ crc_tmp[4] ⊕ data[1] ⊕ data[4] ⊕ data[6] ⊕ data[7]
crc[2] = crc_tmp[0] ⊕ crc_tmp[3] ⊕ crc_tmp[4] ⊕ data[0] ⊕ data[2] ⊕ data[3] ⊕ data[6] ⊕ data[7]
crc[3] = crc_tmp[0] ⊕ crc_tmp[1] ⊕ crc_tmp[4] ⊕ data[1] ⊕ data[4] ⊕ data[3] ⊕ data[7]
crc[4] = crc_tmp[1] ⊕ crc_tmp[2] ⊕ data[2] ⊕ data[4] ⊕ data[5]

The above calculation formula can be abstracted as a switch matrix shown in Figure 4.4-3:

Figure 4.4-3. CRC Calculation Matrix

Note:
The CRC calculation described above is a Linear Feedback Shift Register (LFSR) implementation of the bytewise CRC algorithm. The formulas can be generated with some online tools according to the polynomial and the data width for parallel computation (always 8 bits for ESP32-P4).

4.5 Event Task Matrix Feature

The GDMA controller on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows GDMA's ETM tasks to be triggered by any peripherals' ETM events, or GDMA's ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to GDMA. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

GDMA can receive the following ETM tasks:

• GDMA_AHB/AXI_TASK_IN_START_CHn: Enables the corresponding RX channel n for data transfer.
• GDMA_AHB/AXI_TASK_OUT_START_CHn: Enables the corresponding TX channel n for data transfer.
```