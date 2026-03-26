

```markdown
Note that if two or more private keys with the same key_purpose are restored, only the last one will take effect.
For more information about key_purpose, see Section 4.

34.6.2.6 key_info Export Mode

After successfully deploying the private key, users can regenerate key_info and obtain it with the help of this mode.

The specific process is as follows.

1. Select the successfully deployed key_purpose to enter the key_info export mode.
2. Wait for the Key Manager process to complete.
3. Read key_info from the internal memory of the Key Manager.

Note:

* This mode can be used to output different key_info for the same key.
* This mode can also only update HUK without updating the private key. The detailed operation is:
    - Update the HUK using the HUK Generation Mode.
    - Update the key_info through the key_info Export Mode.
By such way, the chip in the next startup can use the new key_info to restore the same private key under the new HUK.

34.7 Programming Procedures

34.7.1 HUK Generator

The HUK generation process is divided into six phases:

1. IDLE: In this phase, users configure the mode and static parameters.
2. PREP: In this phase, HUK_STATE is BUSY. The HUK Generator prepares for HUK generation. Users need to wait for this phase to complete. The HUK Generator will automatically proceed to the LOAD phase.
3. LOAD: In this phase, users store the HUK information into the internal memory of the HUK Generator based on the selected mode.
4. PROC: In this phase, HUK_STATE is BUSY. The HUK Generator performs the HUK generation process. Users need to wait for the phase to complete. The HUK Generator will automatically proceed to the GAIN phase.
5. GAIN: In this phase, users read the required HUK information from the internal memory of the HUK Generator based on the selected mode.
6. POST: In this phase, HUK_STATE is BUSY. The HUK Generator completes the follow-up tasks for HUK generation. Users need to wait for this phase to complete. The HUK Generator will automatically return to the IDLE phase.
```