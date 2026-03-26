

```markdown
(d) Wait for the HUK Generator to return to the IDLE phase.

3. Configure Key Manager for Private Key Recovery Mode:

(a) Configure the IDLE phase and set KEYMNG_KEY_PURPOSE as flash_128_key, then configure KEYMNG_START.

(b) After entering the LOAD phase, write key_info into the Key Manager, then configure KEYMNG_CONTINUE.

(c) After entering the GAIN phase, configure KEYMNG_CONTINUE.

(d) Wait for the Key Manager to return to the IDLE phase.

4. Enter Encrypted Program Segment:

At this point, the encryption/decryption private key in the external memory has taken effect, and the system enters the encrypted program segment.
```

## 34.9 Interrupts

ESP32-P4's Key Manager and HUK Generator can generate the following interrupt signals that will be sent to the Interrupt Matrix.

* KEYMNG_INTR
* HUK_INTR

There are several internal interrupt sources from Key Manager and HUK Generator that can generate the above interrupt signals. The interrupt sources from Key Manager and HUK Generator are listed with their trigger conditions and the resulted interrupt signals in Table 34.9-1.

Table 34.9-1. Key Manager and HUK Generator's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
|----------------------------|-------------------|------------------|
| KEYMNG_PREP_DONE_INT       | Completion of Key Manager's PREP phase | KEYMNG_INTR |
| KEYMNG_PROC_DONE_INT       | Completion of Key Manager's PROC phase | KEYMNG_INTR |
| KEYMNG_POST_DONE_INT       | Completion of Key Manager's POST phase | KEYMNG_INTR |
| HUK_PREP_DONE_INT          | Completion of HUK Generator's PREP phase | HUK_INTR |
| HUK_PROC_DONE_INT          | Completion of HUK Generator's PROC phase | HUK_INTR |
| HUK_POST_DONE_INT          | Completion of HUK Generator's POST phase | HUK_INTR |

**Note:**

For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.

## 34.10 Memory Blocks

The addresses in this section are relative to Key Manager or HUK Generator base address provided in Table 7.3-2 in Chapter 7 System and Memory.
```