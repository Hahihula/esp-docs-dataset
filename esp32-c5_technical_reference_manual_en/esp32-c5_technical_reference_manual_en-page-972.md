

```markdown
3. Wait for Manual Encryption block to be idle. Poll register XTS_AES_STATE_REG until it reads 0 which indicates the Manual Encryption block is idle.
4. Trigger manual encryption by writing 1 to register XTS_AES_TRIGGER_REG.
5. Wait for the encryption process completion. Poll register XTS_AES_STATE_REG until it reads 2. Step 1 to 5 are the steps of encrypting plaintext instructions/data with the Manual Encryption block using the Key.
6. Write 1 to register XTS_AES_RELEASE_REG to grant SPI1 the access to the encrypted ciphertext. After this, the value of register XTS_AES_STATE_REG will become 3.
7. Call SPI1 to write the ciphertext in the external flash (see Section API Reference - Flash Encrypt in ESP-IDF Programming Guide).
8. Write 1 to register XTS_AES_DESTROY_REG to destroy the ciphertext. After this, the value of register XTS_AES_STATE_REG will become 0.

Repeat the above steps according to the amount of plaintext instructions/data that need to be encrypted.
```

## 29.6 Anti-DPA

DPA (Differential Power Analysis) is a side-channel attack method in cryptography, through which an attacker can statistically analyze data collected from multiple encryption operations to calculate intermediate values in the encryption computation. ESP32-C5 XTS_AES supports two Anti-DPA methods to defend against external DPA attacks.

The XTS-AES algorithm can be divided into two steps, according to IEEE Std 1619-2007:

* Step 1: Calculating Tweak value.
* Step 2: Calculating Cipher/Plain text. In this section, we define this step as calculating Data units.

ESP32-C5 allows users to enable anti-DPA function separately during the above-mentioned two steps to enhance security. See details in the following sections.

### 29.6.1 Clock Anti-DPA Function

Clock Anti-DPA function is the first method to defend against external DPA attacks. Different security levels can be configured through registers:

* First we define the below parameters for a better description:
    - `select_reg = XTS_AES_CRYPT_DPA_SELECT_REGISTER`
    - `reg_d_dpa_en = XTS_AES_CRYPT_CALC_D_DPA_EN`
    - `efuse_dpa_en = EFUSE_CRYPT_DPA_ENABLE`
    - `reg_anti_dpa_level = XTS_AES_CRYPT_SECURITY_LEVEL`
    - `efuse_anti_dpa_level = 3`

* Configure the security level of Anti-DPA for the XTS_AES module:

```markdown
Anti_DPA_level = select_reg ? (reg_anti_dpa_level) : (efuse_dpa_en * efuse_anti_dpa_level)
```
```