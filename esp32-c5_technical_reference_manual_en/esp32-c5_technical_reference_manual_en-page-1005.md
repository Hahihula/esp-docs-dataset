

```markdown
Chapter 31 Key Manager

GoBack

(a) If using software to configure init_key: write sw_init_key (256 bits) into KEYMNG_SW_INIT_KEY_MEM.
(b) Write k2_info (512 bits) into KEYMNG_ASSIST_INFO_MEM.
(c) Write k1_encrypted (256 bits) into KEYMNG_PUBLIC_INFO_MEM.

• ECDHO Deploy Mode:
  (a) Write k1 * G (512 bits) into KEYMNG_PUBLIC_INFO_MEM.

• ECDH1 Deploy Mode:
  (a) If the software configured init_key is used: write sw_init_key (256 bits) into KEYMNG_SW_INIT_KEY_MEM.
  (b) Write k2_info (512 bits) into KEYMNG_ASSIST_INFO_MEM.
  (c) Write k1 * G (512 bits) into KEYMNG_PUBLIC_INFO_MEM.

• Private Key Recovery Mode:
  (a) Write key_info (512 bits) into KEYMNG_ASSIST_INFO_MEM.

• key_info Export Mode: No additional configuration is required.

2. Transition to PROC Phase: Configure KEYMNG_CONTINUE to complete the LOAD phase and enter the PROC phase.

31.7.2.4 PROC Phase

Users need to wait for the PROC phase to complete. This can be done using one of the following methods.

• Monitor KEYMNG_STATE: Continuously check KEYMNG_STATE until it is no longer BUSY.
• Use Interrupt: Enable the interrupt KEYMNG_PROC_DONE_INT and handle the completion in the interrupt service routine.

31.7.2.5 GAIN Phase

Users check KEYMNG_STATE to confirm that the Key Manager is in the GAIN phase. In the GAIN phase, users extract the required key information based on the selected mode of the Key Manager.

1. Extract Key Information:

• Random Deploy Mode:
  (a) Read key_info (512 bits) from KEYMNG_PUBLIC_INFO_MEM.

• AES Deploy Mode:
  (a) Read key_info (512 bits) from KEYMNG_PUBLIC_INFO_MEM.

• ECDHO Deploy Mode:
  (a) Read key_info (512 bits) from KEYMNG_PUBLIC_INFO_MEM.
  (b) Read k2 * G (512 bits) from KEYMNG_ASSIST_INFO_MEM.

• ECDH1 Deploy Mode:

Espressif Systems
1005
ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```