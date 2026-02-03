**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

**GoBack**

- **By RTC GPIO:** set `RTC_CNTL_ULP_CP_GPIO_WAKEUP_ENA`. For more information, see Chapter 10 Low-power Management (`RTC_CNTL`).

6. Set the system into sleep mode.

When the system is in Deep-sleep mode:

1. The timer periodically sets the low-power controller (see [Chapter 10 Low-power Management](RTC_CNTL)) to Monitor mode and then wakes up the coprocessor.
2. Coprocessor executes some necessary operations, such as monitoring external environment via low-power sensors.

3. After the operations are finished, the system goes back to Deep-sleep mode.

4. ULP coprocessor goes back to halt mode and waits for next wakeup.

In monitor mode, ULP coprocessor is woken up and goes to halt as shown in Figure 2.4-1.

![Figure 2.4-1. ULP Sleep and Wakeup Sequence](image)

1. Enable the timer and the timer starts counting.
2. The timer expires and wakes up the ULP coprocessor. ULP coprocessor starts running and executes the program flashed in RTC slow memory.
3. ULP coprocessor goes to halt and the timer starts counting again.

- Put `ULP-RISC-V` into HALT: set `RTC_CNTL_COCPU_DONE`.
- Put `ULP-FSM` into HALT: execute HALT instruction.

4. Disable the timer by ULP program or by software. ULP coprocessor exits from monitor mode.
   - Disabled by software: clear `RTC_CNTL_ULP_CP_SLP_TIMER_EN`.
   - Disabled by RTC GPIO: clear `RTC_CNTL_ULP_CP_GPIO_WAKEUP_ENA` and set `RTC_CNTL_ULP_CP_GPIO_WAKEUP_CLR`.

**Note:**
- If the timer is enabled by software (RTC GPIO), it should be disabled by software (RTC GPIO).
- Before setting ULP-RISC-V to HALT, users should configure `RTC_CNTL_COCPU_DONE` first, therefore, it is recommended to end the flashed program with the following pattern:
  - Set `RTC_CNTL_COCPUDone` to end the operation of ULP-RISC-V and put it into halt.

**Footer:**
Espressif Systems
308 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback