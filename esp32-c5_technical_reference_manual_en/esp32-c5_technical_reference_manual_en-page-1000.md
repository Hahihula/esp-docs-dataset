

```markdown
2. Transition to PREP Phase: Set HUK_START to complete the IDLE phase and enter the PREP phase.

31.71.2 PREP Phase

Users need to wait for the PREP phase to complete. This can be accomplished using one of the following methods:

* Monitor HUK_STATE: Continuously check HUK_STATE until it is no longer BUSY.
* Use Interrupts: Enable the interrupt HUK_PREP_DONE_INT and handle the completion in the interrupt service routine.

31.71.3 LOAD Phase

Users check HUK_STATE to confirm that the HUK Generator is in the LOAD phase. In the LOAD phase, users need to perform the following configurations.

1. Configure Based on Mode: Depending on the mode of the HUK Generator, configure as follows:

    * HUK Generation Mode: No additional configuration is required.
    * HUK Recovery Mode: Write the HUK recovery information (huk_info, 96 words) into HUK_INFO_MEM.

Note:
If multiple huk_info have been generated and stored in external memory previously, using any huk_info in the HUK Recovery Mode will restore its corresponding HUK.

2. Transition to PROC Phase: Set the bit HUK_CONTINUE to 1 to complete the LOAD phase and enter the PROC phase.

31.71.4 PROC Phase

Users need to wait for the PROC phase to complete. This can be done using one of the following methods.

* Monitor HUK_STATE: Continuously check HUK_STATE until it is no longer BUSY.
* Use Interrupts: Enable the interrupt HUK_PROC_DONE_INT and handle the completion in the interrupt service routine.

31.71.5 GAIN Phase

Users check HUK_STATE to confirm that the HUK Generator is in the GAIN phase. In the GAIN phase, users extract the required key information based on the selected mode of the HUK Generator.

1. Extract Key Information:

    * HUK Generation Mode: Read huk_info (185 words) from HUK_INFO_MEM.
    * HUK Recovery Mode: Update huk_info (185 words), depending on HUK_UPDATE_REQ:
        - 0: Do not need to update huk_info, or read any information.
        - 1: Must update huk_info by reading a new value (185 words) from HUK_INFO_MEM.
```