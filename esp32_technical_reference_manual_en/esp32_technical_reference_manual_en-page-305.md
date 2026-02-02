Title: Chapter 17 External Memory Encryption and Decryption (FLASH)

Subtitle: GoBack

Section Title: **17.3.2 Flash Encryption Block**

Body Text:
The Flash Encryption block is equipped with registers that can be accessed by the CPU directly. Registers embedded in the Flash Encryption block, registers in the peripheral DPort register, system parameters and Boot Mode jointly configure and control this block.

The Flash Encryption block requires software intervention during operation. The steps are as follows:

1. Set the DPOR_SPI_ENCRYPT_ENABLE bit of register DPOR_SLAVE_SPI_CONFIG_REG.
2. Write the physical address prepared for the off-chip flash on register FLASH_ENCRYPT_ADDRESS_REG. The address must be 8-word boundary aligned.
3. The Flash Encryption block must encrypt 8-word long code segments. Write the lowest word to register FLASH_ENCRYPT_BUFFER_0_REG, the second-lowest word into FLASH_ENCRYPT_BUFFER_1_REG, and so on, up to FLASH_ENCRYPT_BUFFER_7_REG.

4. Set the FLASH_START bit in FLASH_ENCRYPT_START_REG.
5. Wait for the FLASH_DONE bit to be set in FLASH_ENCRYPT_DONE_REG.
6. Use this function and write any 8-word code to the 8-word aligned address on the off-chip flash via the peripheral SPI0.

In Steps 1 to 5, the Flash Encryption block encrypts 8-word long codes. The key encryption algorithm uses Keye. The encryption result will also be 8-word long. In Step 6, the peripheral SPI0 writes encrypted results of the Flash Encryption block to the off-chip flash. One parameter of the function used in Step 6 will be the physical address of the off-chip flash. The physical address must be 8-word boundary aligned. Also, the value must be the same as the value written into register FLASH_ENCRYPT_ADDRESS_REG during Step 2. Even though the function used in Step 6 still has a parameter with an 8-word long code, the parameter will be meaningless if Steps 1 to 5 are executed. The Peripheral SPI0 will use the encrypted result instead. If the Flash Encryption block is not operating, or has not executed Steps 1 to 5, Step 6 will not use the encrypted result. Instead, the function parameter will be used.

Flash Encryption Operating Conditions:

- During SPI Flash Boot
  - If the DPOR_SPI_ENCRYPT_ENABLE bit of register DPOR_SLAVE_SPI_CONFIG_REG is 1, the Flash Encryption block is operational. Otherwise, it is not.
  
- During Download Boot
  - If the DPOR_SPI_ENCRYPT_ENABLE bit of register DPOR_SLAVE_SPI_CONFIG_REG is 1, and system parameter download_dis_encrypt is 0, the Flash Encryption block is operational. Otherwise, it is not.

Even though software participates in the whole process, it cannot directly read the encrypted codes. Instead, the encrypted codes are integrated into the off-chip flash. Even though the CPU can skip the cache and get the encrypted code directly by reading the off-chip flash, the software can by no means access Keye.

Section Title: **17.3.3 Flash Decryption Block**

Body Text:
Flash Decryption is not a conventional peripheral, and is not equipped with registers. Therefore, the CPU cannot directly access the Flash Decryption block. The Peripheral DPort Register, system parameters and Booting Mode jointly control and configure the Flash Decryption block.

Footer: Espressif Systems  
Page Number: 305  
Document Version: ESP32 TRM (Version 5.6)  
Link Text: Submit Documentation Feedback