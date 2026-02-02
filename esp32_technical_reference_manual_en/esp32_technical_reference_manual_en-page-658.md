**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Heading:**  
29.3.2.4 PWM Timer Synchronization and Phase Locking

**Body Text:**
The PWM modules adopt a flexible synchronization method. Each PWM timer has a synchronization input and a synchronization output. The synchronization input can be selected from three synchronization outputs and three synchronization signals from the GPIO matrix. The synchronization output can be generated from the synchronization input signal, or when the PWM timer’s value is equal to period or zero. Thus, the PWM timers can be chained together with their phase locked. During synchronization, the PWM timer clock prescaler will reset its counter in order to synchronize the PWM timer clock.

**Subsection Heading:**  
29.3.3 PWM Operator Submodule

**Body Text:**
The PWM Operator submodule has the following functions:
- Generates a PWM signal pair, based on timing references obtained from the corresponding PWM timer.
- Each signal out of the PWM signal pair includes a specific pattern of dead time.
- Superimposes a carrier on the PWM signal, if configured to do so.

**Body Text:**
Handles response under fault conditions. 

**Figure Caption:**  
Figure 29.3-13 shows the block diagram of a PWM operator.

**Subsection Heading:**  
29.3.3.1 PWM Generator Submodule

**Subtitle:**  
Purpose of the PWM Generator Submodule

**Body Text:**
In this submodule, important timing events are generated or imported. The events are then converted into specific actions to generate the desired waveforms at the PWMxA and PWMxB outputs.

**Footer Information:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:**  
658