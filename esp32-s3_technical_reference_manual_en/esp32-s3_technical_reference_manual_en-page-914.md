**Chapter Title:**
Chapter 23 External Memory Encryption and Decryption (XTS_AES)

**GoBack**

**Body Text with Code Snippet:**
```
If bit SYSTEM_ENABLE_DOWNLOAD_GOCD_DECRYPT in register 
SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG is 1, the Auto Decryption block can be enabled. Otherwise, it is not operational.
```

**Note Section:**
- When the Auto Decryption block is enabled, it will automatically decrypt the ciphertext if the CPU reads instructions/data from the external memory via cache to retrieve the instructions/data. The entire decryption process does not need software participation and is transparent to the cache. Users can by no means obtain the decryption Key during the process.
- When the Auto Decryption block is disabled, it does not have any effect on the contents stored in the external memory, no matter they are encrypted or not. Therefore, what the CPU reads via cache is the original information stored in the external memory.

**Subheading:**
23.5 Software Process

**Body Text with Steps and Instructions for Manual Encryption Block Operation (continued):**

When the Manual Encryption block operates, software needs to be involved in the process. The steps are as follows:

1. **Configure XTS_AES:**
   - Set register XTS_AES_DESTINATION_REG to type = 0.
   - Set register XTS_AES_PHYSICAL_ADDRESS_REG to base_addr.
   - Set register XTS_AES_LINESIZE_REG to size/32.

For definitions of type, base_addr and size, please refer to Section 23.4.3.

2. **Pad plaintext data:**
   - Pad plaintext data to the registers block XTS_AESPLAIN_n_REG (n: 0-15). For detailed information, please refer to Section 23.4.4.
   - Please pad data according to your actual needs, and the unused ones could be set to arbitrary values.

3. **Wait for Manual Encrypt block idle status:** 
   - Poll register XTS_AES_STATE_REG until the software reads 0.

4. **Trigger manual encryption:**
   - By writing 1 to register XTS_AES_TRIGGER_REG.

5. **Wait for encryption process completion:**
   - Poll register XTS_AES_STATE_REG until the software reads 2.
   Step 1 to 5 are the steps of encrypting plaintext instructions with the Manual Encryption block using the Key.

6. **Grant the ciphertext access:** 
   - Write 1 to register XTS_AES_RELEASE_REG to grant SPI1 the access to the encrypted ciphertext after this, the value of register XTS_AES_STATE_REG will become 3.
   
7. **Call SPI1:**
   - To write the ciphertext in the external flash (see Chapter 30 SPI Controller (SPI)).

8. **Destroy the ciphertext:** 
   - Write 1 to register XTS_AES_DESTROY_REG. After this, the value of register XTS_AES_STATE_REG will become 0.
   
Repeat above steps to meet plaintext instructions/data encryption demands.

**Footer:**
Espressif Systems
Submit Documentation Feedback

914 ESP32-S3 TRM (Version 1.7)