

# Chapter 31

## LED PWM Controller (LEDC)

### 31.1 Overview

The LED PWM Controller is a peripheral designed to generate PWM signals for LED control. It has specialized features such as automatic duty cycle fading. However, the LED PWM Controller can also be used to generate PWM signals for other purposes.

### 31.2 Features

The LED PWM Controller has the following features:

* Six independent PWM generators (i.e., six channels)
* Maximum PWM duty cycle resolution: 20 bits
* Four independent timers that support fractional division
* Adjustable phase of PWM signal output
* PWM duty cycle dithering
* Automatic duty cycle fading — gradual increase/decrease of a PWM's duty cycle without interference from the processor. An interrupt will be generated upon fade completion
* Up to 16 duty cycle ranges for each PWM generator to generate gamma curve signals - each range can be independently configured in terms of fading direction (increase or decrease), fading amount (the amount by which the duty cycle increases or decreases each time), the number of fades (how many times the duty cycle fades in one range), and fading frequency
* PWM signal output in low-power mode (Light-sleep mode)
* Event generation and task response related to the Event Task Matrix (ETM) peripheral

Note that the four timers are identical regarding their features and operation. The following sections refer to the timers collectively as Timerx (where x ranges from 0 to 3). Likewise, the six PWM generators are also identical in features and operation, and thus are collectively referred to as PWMn (where n ranges from 0 to 5).

### 31.3 Architectural Overview

Figure 31.3-1 shows the architecture of the LED PWM Controller.