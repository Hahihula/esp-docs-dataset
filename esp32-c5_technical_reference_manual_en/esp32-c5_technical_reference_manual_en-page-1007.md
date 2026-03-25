

```markdown
Chapter 31 Key Manager

GoBack

(a) Configure the IDLE phase, set KEYMNG_KEY_PURPOSE as XTS, and configure KEYMNG_START.
(b) After entering the LOAD phase, write the locally generated k1 * G to the Key Manager, then configure KEYMNG_CONTINUE.
(c) After entering the GAIN phase, read out key_info and k2 * G, then configure KEYMNG_CONTINUE.
(d) Wait for the Key Manager to return to the IDLE phase.

5. Upload Key: Upload k2 * G to the user through the communication interface.

6. Generate and Encrypt Data:
  - Generate the negotiated private key k1 * k2 * G based on the obtained k2 * G and the local k1.
  - Encrypt data locally and write the ciphertext to flash.

31.8.2 Software Process in Chip Normal Startup Phase

Once the chip has been deployed, the complete process for a normal startup is as follows.

1. Start in SPI Boot Mode:
   The chip begins in SPI boot mode and first enters the unencrypted program segment.

2. Configure HUK Recovery Mode:
   Since the HUK has been generated, configure the HUK Recovery Mode as follows:
   (a) Configure the IDLE phase and set the working mode as Huk Recovery Mode as specified in Table 31.6-1, then configure HUK_START.
   (b) After entering the LOAD phase, write huk_info into the HUK Generator, then configure HUK_CONTINUE.
   (c) After entering GAIN phase, configure HUK_CONTINUE.
   (d) Wait for the HUK Generator to return to the IDLE phase.

3. Configure Key Manager for Private Key Recovery Mode:
   (a) Configure the IDLE phase and set KEYMNG_KEY_PURPOSE as XTS, then configure KEYMNG_START.
   (b) After entering the LOAD phase, write key_info into the Key Manager, then configure KEYMNG_CONTINUE.
   (c) After entering the GAIN phase, configure KEYMNG_CONTINUE.
   (d) Wait for the Key Manager to return to the IDLE phase.

4. Enter Encrypted Program Segment:
   At this point, the encryption/decryption private key in the external memory has taken effect, and the system enters the encrypted program segment.

31.9 Interrupts

ESP32-C5’s Key Manager and HUK Generator can generate the following interrupt signals that will be sent to the Interrupt Matrix.
```