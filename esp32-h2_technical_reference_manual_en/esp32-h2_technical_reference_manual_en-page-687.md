

```markdown
For definitions of `base_addr` and `size`, please refer to Section 26.4.3.

2. Write plaintext instructions/data to the registers block XTS_AES_PLAIN_n_REG (n: 0-15). For detailed information, please refer to Section 26.4.4.
   Please write data to registers according to your actual needs, and the unused ones could be set to arbitrary values.

3. Wait for Manual Encryption block to be idle. Poll register XTS_AES_STATE_REG until it reads 0 which indicates the Manual Encryption block is idle.

4. Trigger manual encryption by writing 1 to register XTS_AES_TRIGGER_REG.

5. Wait for the encryption process completion. Poll register XTS_AES_STATE_REG until it reads 2.
   Step 1 to 5 are the steps of encrypting plaintext instructions/data with the Manual Encryption block using the Key.

6. Write 1 to register XTS_AES_RELEASE_REG to grant SPI1 the access to the encrypted ciphertext. After this, the value of register XTS_AES_STATE_REG will become 3.

7. Call SPI1 to write the ciphertext in the external flash (see Section API Reference - Flash Encrypt in ESP-IDF Programming Guide).

8. Write 1 to register XTS_AES_DESTROY_REG to destroy the ciphertext. After this, the value of register XTS_AES_STATE_REG will become 0.
Repeat the above steps according to the amount of plaintext instructions/data that need to be encrypted.

## 26.6 Anti-DPA

DPA (Differential Power Analysis) is a side-channel attack method in cryptography, through which an attacker can statistically analyze data collected from multiple encryption operations to calculate intermediate values in the encryption computation. ESP32-H2 XTS_AES supports two Anti-DPA methods to defend against external DPA attacks.

The XTS-AES algorithm can be divided into two steps, according to IEEE Std 1619-2007:

* Step 1: Calculating Tweak value.
* Step 2: Calculating Cipher/Plain text. In this section, we define this step as calculating Data units.

ESP32-H2 allows users to enable anti-DPA function separately during the above-mentioned two steps to enhance security. See details in the following sections.

### 26.6.1 Clock Anti-DPA Function

Clock Anti-DPA function is the first method to defend against external DPA attacks. Different security levels can be configured through registers:

* First we define the below parameters for a better description:
    - `select_reg = XTS_AES_CRYPT_DPA_SELECT_REGISTER`
    - `reg_d_dpa_en = XTS_AES_CRYPT_CALC_D_DPA_EN`
    - `efuse_dpa_en = EFUSE_CRYPT_DPA_ENABLE`
```