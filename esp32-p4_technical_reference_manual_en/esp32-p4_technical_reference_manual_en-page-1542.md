

```markdown
Chapter 32 External Memory Encryption and Decryption (XTS_AES) GoBack

1. Configure XTS_AES:
   - Set register `XTS_AES_DESTINATION_REG` to `type = 0`.
   - Set register `XTS_AES_PHYSICAL_ADDRESS_REG` to `base_addr`.
   - Set register `XTS_AES_LINESIZE_REG` to `$\frac{size}{32}$`.

   For definitions of `base_addr` and `size`, please refer to Section 32.4.3.

2. Write plaintext instructions/data to the registers block `XTS_AES_PLAIN_n_REG` (n: 0-15). For detailed information, please refer to Section 32.4.4.
   Please write data to registers according to your actual needs, and the unused ones could be set to arbitrary values.

3. Wait for Manual Encryption block to be idle. Poll register `XTS_AES_STATE_REG` until it reads 0 which indicates the Manual Encryption block is idle.

4. Trigger manual encryption by writing 1 to register `XTS_AES_TRIGGER_REG`.

5. Wait for the encryption process completion. Poll register `XTS_AES_STATE_REG` until it reads 2.
   Step 1 to 5 are the steps of encrypting plaintext instructions/data with the Manual Encryption block using the Key.

6. Write 1 to register `XTS_AES_RELEASE_REG` to grant SPI1 the access to the encrypted ciphertext. After this, the value of register `XTS_AES_STATE_REG` will become 3.

7. Call SPI1 to write the ciphertext in the external flash (see Section API Reference - Flash Encrypt in ESP-IDF Programming Guide).

8. Write 1 to register `XTS_AES_DESTROY_REG` to destroy the ciphertext. After this, the value of register `XTS_AES_STATE_REG` will become 0.

Repeat the above steps according to the amount of plaintext instructions/data that need to be encrypted.

32.6 Anti-DPA

DPA (Differential Power Analysis) is a side-channel attack method in cryptography, through which an attacker can statistically analyze data collected from multiple encryption operations to calculate intermediate values in the encryption computation. ESP32-P4 XTS_AES supports Anti-DPA to defend against external DPA attacks.

The XTS-AES algorithm can be divided into two steps, according to IEE Std 1619-2007:

   - Step 1: Calculating T value. In this section, we define this step as "calculating T".
   - Step 2: Calculating Cipher/Plain text. In this section, we define this step as "calculating D".

Different security levels can be configured through registers:

   - First we define the below parameters for a better description:
     - `select_reg = XTS_AES_CRYPT_DPA_SELECT_REGISTER`
     - `reg_d_dpa_en = XTS_AES_CRYPT_CALC_D_DPA_EN`
     - `efuse_dpa_en = EFUSE_CRYPT_DPA_ENABLE`

Espressif Systems          1542
Submit Documentation Feedback ESP32-P4 TRM PRELIMINARY
```