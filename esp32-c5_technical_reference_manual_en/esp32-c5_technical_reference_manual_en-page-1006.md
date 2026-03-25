

```markdown
Chapter 31 Key Manager

GoBack

(a) Read key_info (512 bits) from KEYMNG_PUBLIC_INFO_MEM.
• Private Key Recovery Mode: no need to read any information.
• key_info Export Mode:
    (a) Read key_info (512 bits) from KEYMNG_PUBLIC_INFO_MEM.

2. Transition to POST Phase: Configure KEYMNG_CONTINUE to complete the GAIN phase and enter the POST phase.

31.7.2.6  POST Phase

Users need to wait for the POST phase to complete. This can be done using one of the following methods.
• Monitor KEYMNG_STATE: Continuously check KEYMNG_STATE until it is no longer BUSY.
• Use Interrupt: Enable the interrupt KEYMNG_POST_DONE_INT and handle the completion in the interrupt service routine.

31.8 Programming Examples

Based on the previous sections, we can outline a comprehensive chip deployment process. This section explains the operation procedures for the HUK Generator and Key Manager during two typical chip startup scenarios.

Note:
In this section, all configuration processes are described in a simplified manner. For detailed instructions, please refer to Section 31.7.

31.8.1 Software Process in Chip Private Key Deploy Phase

The following steps outline the process for booting up the chip for the first time and deploying the private key for encrypting and decrypting external memory.

1. Enter Download Mode: The chip enters the download mode.
2. Configure HUK Generator: Since it is the first time to start the chip, configure the HUK Generator to enter the HUK Generation Mode.
    (a) Configure the IDLE phase and set the working mode as HUK Generation Mode as specified in Table 31.6-1, then configure HUK_START.
    (b) After entering the LOAD phase, configure HUK_CONTINUE.
    (c) After entering GAIN phase, read out huk_info, then configure HUK_CONTINUE.
    (d) Wait for the HUK Generator to return to the IDLE phase.
3. Set HUK Generation State: Write EFUSE_KM_HUK_GEN_STATE to make the total number of bits set to 1 is odd, so that the HUK Generator will work only in HUK Recovery Mode during subsequent startups.
4. Configure Key Deployment: Take the key deployment in ECDHO Deploy Mode as an example.

Espressif Systems    1006
ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```