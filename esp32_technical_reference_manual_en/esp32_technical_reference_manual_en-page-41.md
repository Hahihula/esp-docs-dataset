**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Body Text:**

(PCM) which is stored in register SENS_PC_INIT. The relationship between the described signals and registers is shown in Figure 1.5-1.

On reset or power-up the above-mentioned ULP program may start up only after the expiration of SENS_ULP_CP_SLEEP_CYCO_REG, which is the default selection period of the ULP timer.

A sample operation sequence of the ULP program is shown in Figure 1.5-2, where the following steps are executed:

1. Software enables the ULP timer by using bit RTC_CNTL_ULP_CP_SLP_TIMER_EN.
2. The ULP timer expires and the ULP coprocessor starts running the program at PC = SENS_PC_INIT.
3. The ULP program executes the HALT instruction; the ULP coprocessor is halted and the timer gets restarted.
4. The ULP program executes the SLEEP instruction to change the sleep timer period register.
5. The ULP program, or software, disables the ULP timer by using bit RTC_CNTL_ULP_CP_SLP_TIMER_EN.

**Figure 1.5-2: Sample of a ULP Operation Sequence**

The specific timing of the wakeup, program execution and sleep sequence is governed by the ULP FSM as follows:

1. On the ULP timer expiration the FSM wakes up the ULP and this process takes two clock cycles.
2. Then, before executing the program, the FSM waits for the number of cycles configured in RTC_CNTL_ULPCP_TOUCH_START_WAIT field of the RTC_CNTL_TIMER2_REG register. This time is spent waiting for the 8 MHz clock to get stable.
3. The ULP program is executed.
4. After calling HALT instruction, the program is stopped. The FSM requires additional two clock cycles to put the ULP to sleep.

**Subsection Title:**
1.6 RTC_I2C Controller

The ULP coprocessor can use a separate I2C controller, located in the RTC domain, to communicate with external I2C slave devices. RTC_I2C has a limited feature set, compared to I2C0/I2C1 peripherals.

**Footer:**
Espressif Systems  
41  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback