

```markdown
Chapter 34 Key Manager

GoBack

## 34.8.1 Software Process in Chip Private Key Deploy Phase

The following steps outline the process for booting up the chip for the first time and deploying the private key for encrypting and decrypting external memory.

1. Enter Download Mode: The chip enters the download mode.
2. Configure HUK Generator: Since it is the first time to start the chip, configure the HUK Generator to enter the HUK Generation Mode.
   (a) Configure the IDLE phase and set the working mode as HUK Generation Mode as specified in Table 34.6-1, then configure `HUK_START`.
   (b) After entering the LOAD phase, configure `HUK_CONTINUE`.
   (c) After entering GAIN phase, read out `huk_info`, then configure `HUK_CONTINUE`.
   (d) Wait for the HUK Generator to return to the IDLE phase.
3. Set HUK Generation State: Write `EFUSE_KM_HUK_GEN_STATE` to make the total number of bits set to 1 is odd, so that the HUK Generator will work only in HUK Recovery Mode during subsequent startups.
4. Configure Key Deployment: Take the key deployment in ECDHO Deploy Mode as an example.
   (a) Configure the IDLE phase, set `KEYMNG_KEY_PURPOSE` as XTS, and configure `KEYMNG_START`.
   (b) After entering the LOAD phase, write the locally generated `k1 * G` to the Key Manager, then configure `KEYMNG_CONTINUE`.
   (c) After entering the GAIN phase, read out `key_info` and `k2 * G`, then configure `KEYMNG_CONTINUE`.
   (d) Wait for the Key Manager to return to the IDLE phase.
5. Upload Key: Upload `k2 * G` to the user through the communication interface.
6. Generate and Encrypt Data:
   - Generate the negotiated private key `k1 * k2 * G` based on the obtained `k2 * G` and the local `k1`.
   - Encrypt data locally and write the ciphertext to flash.

## 34.8.2 Software Process in Chip Normal Startup Phase

Once the chip has been deployed, the complete process for a normal startup is as follows.

1. Start in SPI Boot Mode:
   The chip begins in SPI boot mode and first enters the unencrypted program segment.
2. Configure HUK Recovery Mode:
   Since the HUK has been generated, configure the HUK Recovery Mode as follows:
   (a) Configure the IDLE phase and set the working mode as HUK Recovery Mode as specified in Table 34.6-1, then configure `HUK_START`.
   (b) After entering the LOAD phase, write `huk_info` into the HUK Generator, then configure `HUK_CONTINUE`.
   (c) After entering GAIN phase, configure `HUK_CONTINUE`.

Espressif Systems
1574
ESP32-P4 TRM
Submit Documentation Feedback PRELIMINARY
```