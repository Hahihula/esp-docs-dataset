**Chapter Title:**
Chapter 35

**Section Titles and Content:**

1. **LED PWM Controller (LEDC) Overview**
   The LED PWM Controller is a peripheral designed to generate PWM signals for LED control. It has specialized features such as automatic duty cycle fading. However, the LED PWM Controller can also be used to generate PWM signals for other purposes.

2. **Features of the LED PWM Controller:**
   - Eight independent PWM generators (i.e., eight channels)
   - Four independent timers that support division by fractions
   - Automatic duty cycle fading (i.e., gradual increase/decrease of a PWM's duty cycle without interference from the processors) with interrupt generation on fade completion
   - Adjustable phase of PWM signal output
   - PWM signal output in low-power mode (Light-sleep mode)
   - Maximum PWM resolution: 14 bits

3. **Note about Timers and PWM Generators**
   Note that the four timers are identical regarding their features and operation. The following sections refer to the timers collectively as Timerx (where x ranges from 0 to 3). Likewise, the eight PWM generators are also identical in features and operation, and they are collectively referred to as PWMn (where n ranges from 0 to 7).

**Figure:**
- **Figure Title:** Figure 35.2-1. LED PWM Architecture
- The figure shows a block diagram of an LED_PWM architecture with four timers labeled Timer0 through Timer3 connected via a Mux, and each timer is linked to multiple PWM outputs (PWM0-PWM7).

**Footer:**
- "Espressif Systems"
- Page number 1310
- Document version ESP32-S3 TRM (Version 1.7)