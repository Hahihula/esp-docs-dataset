

```markdown
Chapter 23 External Memory Encryption and Decryption (XTS_AES) GoBack

2. Write plaintext data to the registers block XTS_AES_PLAIN_n_REG (n: 0-7). For detailed information, please refer to Section 23.4.4.
Please write data to registers according to your actual needs, and the unused ones could be set to arbitrary values.

3. Wait for Manual Encryption block to be idle. Poll register XTS_AES_STATE_REG until it reads 0 that indicates the Manual Encryption block is idle.

4. Trigger manual encryption by writing 1 to register XTS_AES_TRIGGER_REG.

5. Wait for the encryption process completion. Poll register XTS_AES_STATE_REG until it reads 2.
Step 1 to 5 are the steps of encrypting plaintext instructions with the Manual Encryption block using the Key.

6. Write 1 to register XTS_AES_RELEASE_REG to grant SPI1 the access to the encrypted ciphertext. After this, the value of register XTS_AES_STATE_REG will become 3.

7. Call SPI1 to write the ciphertext in the external flash (see Chapter 27 SPI Controller (SPI)).

8. Write 1 to register
XTS_AES_DESTROY_REG to destroy the ciphertext. After this, the value of register XTS_AES_STATE_REG will become 0.

Repeat above steps according to the amount of plaintext instructions/data that need to be encrypted.
```