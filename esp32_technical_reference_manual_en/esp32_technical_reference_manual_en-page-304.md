**Chapter Title:**
Chapter 17 External Memory Encryption and Decryption (FLASH)

**Section Heading:**
17.3 Functional Description

**Figure Caption with Diagram:**
Figure 17.3-1 Flash Encryption/Decryption Module Architecture

**Body Text:**

The Flash Encryption/Decryption module consists of three parts, namely the Key Generator, Flash Encryption block and Flash Decryption block. The structure of these parts is shown in Figure 17.3-1. The Key Generator is shared by both the Flash Encryption block and the Flash Decryption block, which can function simultaneously.

In the peripheral DPort Register, the register relevant to Flash Encryption/Decryption is
DPORT_SPI_ENCRYPT_ENABLE bit and DPORT_SPI_DECRYPT ENABLE bit in 
DPORT_SLAVE_SPI_CONFIG_REG. The Flash Encryption/Decryption module will fetch six system parameters from the peripheral eFuse Controller. These parameters are: coding_scheme, BLOCK1, flash_crypt_config,
download_dis_encrypt, flash_crypt_cnt, and download_dis_decrypt.

**Subsection Heading with Subheading Numbering:**
17.3.1 Key Generator

**Body Text under Subsection 17.3.1:**

According to system parameters coding_scheme and BLOCK1, the Key Generator will first generate
Key_o = f(coding_scheme, BLOCK1).

Then, according to system parameter flash_crypt_config, and off-chip flash physical addresses Addr_e and Addr_d accessed by the Flash Encryption block and the Flash Decryption block, the Key Generator will respectively figure out that:
Key_e = g(Key_o, flash_crypt_config, Addr_e),
Key_d = g(Key_o, flash_crypt_config, Addr_d).

When all values of system parameter flash_crypt_config are 0, Key_e and Key_d are not relevant to the physical address of the off-chip flash. When all values of system parameter flash_crypt_config are not 0, every 8-word block on the off-chip flash has a dedicated Key_e and Key_d.

**Footer:**
Espressif Systems
304 ESP32 TRM (Version 5.6)
Submit Documentation Feedback