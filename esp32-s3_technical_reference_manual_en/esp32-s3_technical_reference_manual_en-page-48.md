**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:** UA_STATE

**Body Text:**
This special register is dedicated to the EE.FFT.AMS.S16.LD.INCP.UAUP instruction. This register is used to store the non-aligned 128-bit data read from memory. Next time when this instruction is called, the data in this register is concatenated to the newly read non-aligned data and then the result is shifted to obtain the 128-bit aligned data.

**Subsection Header:** 15.2 Fast GPIO Interface

**Body Text:**
ESP32-S3’s Xtensa processor adds two signal ports, i.e., GPIO_OUT and GPIO_IN. You can route signals from the two ports to specified GPIO pins via the GPIO Matrix.

**Sub-subsection Header:** 15.2.1 GPIO_OUT

**Body Text:**
An 8-bit processor output interface. Firstly, configure the 8-bit port signals to specified pins via GPIO Matrix. For core0, their names are pro_alangpio_out~7 or for core1, their names are core1_gpio_out~7. Then you can set certain bits of GPIO_OUT to 1 via instructions EE.WR_MASK_GPIO_OUT and EE.SET_BIT_GPIO_OUT, or set certain bits to 0 via instruction EE.CLR_BIT_GPIO_OUT, so as to pull certain pins to high level or low level.

Using this method, you can get faster response than pulling pins through register configurations.

**Sub-subsection Header:** 15.2.2 GPIO_IN

**Body Text:**
An 8-bit processor input interface. Firstly, configure the 8-bit port signals to specified pins via GPIO Matrix. For core0, their names are pro_alangpio_in0~7. For core1, their names are core1_gpio_in0~7. Then you can read the eight GPIO pin levels and store them to the AR register through instruction EE.GET_GPIO_IN. Using this method, you can get and handle the level changes on GPIO pins faster than reading registers to get pin level status.

**Subsection Header:** 15.3 Data Format and Alignment

**Body Text:**
The current extended instruction set supports 1-byte, 2-byte, 4-byte, 8-byte and 16-byte data formats.
Besides, there is also a 20-byte format: QACC_H and QACC_L. However, there is no direct way to switch the data between the two special registers and memory. You can read and write data of QACC_H and QACC_L via five 4-byte (AR) registers or two 16-byte (QR) registers.

The table lists bit length and alignment information for common data format ('x' indicates that the bit is either 0 and 1). The Xtensa processor uses byte as the smallest unit for addresses stored in memory in all data formats. And little-endian byte order is used, with byte 0 stored in the lowest bit (the right side), as shown in Figure 1.4-3.

**Table Title:** Table 1.5-2. Data Format and Alignment

| Data Format | Length | Aligned Addresses In Memory |
|-------------|--------|---------------------------|
| 1-byte      | 8 bits | xxxx                       |
| 2-byte      | 16 bits| xxx0                       |
| 4-byte      | 32 bits| xx00                       |
| 8-byte      | 64 bits| x000                       |
| 16-byte     | 128 bit| 0000                       |

**Footer:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)