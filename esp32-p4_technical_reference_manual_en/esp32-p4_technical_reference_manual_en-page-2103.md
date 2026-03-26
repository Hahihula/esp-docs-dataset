

```markdown
- When voice activities are not detected in the current frame, the count value of silent_count increases by 1:
  * If the count value of speech_count is greater than LP_I2S_PARAM_MIN_SPEECH_COUNT, and
    - The count value of silent_count is greater than LP_I2S_PARAM_HANGOVER_SILENT, the VAD module transitions to the non-voice activity status and resets both speech_count and silent_count to 0;
    - The count value of silent_count is less than LP_I2S_PARAM_HANGOVER_SILENT, the VAD module maintains the voice activity status.
  * If the count value of speech_count is less than or equal to LP_I2S_PARAM_MIN_SPEECH_COUNT, the VAD module transitions directly to the non-voice activity status and resets speech_count to 0.

- Under the voice activity status, the VAD module pauses updating noise information. When the count value of speech_count exceeds LP_I2S_PARAM_MAX_SPEECH_COUNT, indicating stability in the new environment, it resumes learning and updating noise information.


## Status Registers

The VAD module provides several key operational variables as status registers (read-only) to facilitate user debugging. The status registers include:

* `LP_I2S_VAD_FLAG`: Represents the current voice activity detection status. 1 represents the VAD module is in the voice activity status, while 0 represents it is in the non-voice activity status.
* `LP_I2S_ENERGY_ENOUGH`: Represents whether the current frame passes the energy threshold check. 1 represents the current frame passes the energy threshold check, while 0 represents not pass.
* `LP_I2S_SPEECH_COUNT_OB`: Represents the count value of the voice frame counter, speech_count.
* `LP_I2S_SILENT_COUNT_OB`: Represents the count value of the non-voice frame counter, silent_count.


### 41.4.2 Wake-up Source Configuration

When the VAD module is in the voice activity status, it triggers the wake-up source LP_I2S_WAKEUP. Users can configure the wake-up source (please refer to Chapter 47 LP I2S Controller), enabling the VAD to become one of the wake-up sources for ESP32-P4.


## 41.5 Interrupts

ESP32-P4's VAD module shares the same interrupt signal LP_I2S_INTR with the LP I2S module. The following interrupt sources can generate the interrupt signal:

* `LP_I2S_VAD_DONE_INT`: Triggered when the VAD completes processing one frame of data.
* `LP_I2S_VAD_RESET_DONE_INT`: Triggered when the VAD is reset.

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 41.7 Register Summary.
```