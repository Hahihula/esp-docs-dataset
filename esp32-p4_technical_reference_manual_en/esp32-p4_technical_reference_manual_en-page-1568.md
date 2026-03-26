

```markdown
Chapter 34 Key Manager

GoBack

* HUK Generation Mode: Read huk_info (165 words) from HUK_INFO_MEM.
* HUK Recovery Mode: Update huk_info (165 words), depending on HUK_UPDATE_REQ:
    - 0: Do not need to update huk_info, or read any information.
    - 1: Must update huk_info by reading a new value (165 words) from HUK_INFO_MEM.

2. Transition to POST Phase: Set the bit HUK_CONTINUE to complete the GAIN phase and enter the POST phase.

34.71.6 POST Phase

Users need to wait for the POST phase to complete. This can be done using one of the following methods.

* Monitor HUK_STATE: Continuously check HUK_STATE until it is no longer BUSY.
* Use Interrupts: Enable the interrupt HUK_POST_DONE_INT and handle the completion in the interrupt service routine.

34.7.2 Key Manager

The key deployment process of the Key Manager is divided into six phases:

1. IDLE: In this phase, users configure the mode, key usage, and static parameters.
2. PREP: In this phase, KEYMG_STATE is BUSY. The Key Manager performs the necessary preparations for key deployment. Users need to wait for this phase to complete. The Key Manager will automatically proceed to the LOAD phase.
3. LOAD: In this phase, users store the key information into the internal memory of the Key Manager based on the selected mode.
4. PROC: In this phase, KEYMG_STATE is BUSY. The Key Manager performs the key deployment process. Users need to wait for this phase to complete. The Key Manager will automatically proceed to the GAIN phase.
5. GAIN: In this phase, users read the required key information from the internal memory of the Key Manager based on the selected mode.
6. POST: In this phase, KEYMG_STATE is BUSY. The Key Manager completes the follow-up tasks for key deployment. Users need to wait for this phase to complete. The Key Manager will automatically return to the IDLE phase.

34.7.2.1 IDLE Phase

Users check KEYMNG_STATE to confirm that the Key Manager is in the IDLE phase. In the IDLE phase, users need to perform the following configurations.

1. Complete HUK Generation Process:

    (a) Select one of the following two processes, depending on whether the HUK has been generated or not:
        * If HUK has not been generated: Follow the HUK generation process described in Section 34.7.1.
```