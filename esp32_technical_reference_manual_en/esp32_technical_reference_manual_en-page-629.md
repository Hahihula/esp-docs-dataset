**Chapter Title:**
Chapter 28

**Section Heading:**
LED PWM Controller (LEDC)

**Subsection 1: Introduction**

The LED_PWM controller is primarily designed to control the intensity of LEDs, although it can be used to generate PWM signals for other purposes as well. It has 16 channels which can generate independent waveforms that can be used to drive RGB LED devices. For maximum flexibility, the high-speed as well as the low-speed channels can be driven from one of four high-speed/low-speed timers. The PWM controller also has the ability to automatically increase or decrease the duty cycle gradually, allowing for fades without any processor interference. To increase resolution, the LED_PWM controller is also able to dither between two values, when a fractional PWM value is configured.

The LED_PWM controller has eight high-speed and eight low-speed PWM generators. In this document, they will be referred to as hschn and lscrn, respectively. These channels can be driven from four timers which will be indicated by h_timerx and l_timerx.

**Subsection 2: Functional Description**

**Sub-subsection a: Architecture (Section Heading)**

Figure **28.2-1**: shows the architecture of the LED_PWM controller. As can be seen in the figure, the LED_PWM controller contains eight high-speed and eight low-speed channels. There are four high-speed clock modules for the high-speed channels, from which one h_timerx can be selected. There are also four low-speed clock modules for the low-speed channels, from which l_timerx can be selected.

**Figure Caption:**
Figure 28.2-1 illustrates a PWM channel with its selected timer; in this instance a high-speed channel and associated high-speed timer.
- **Figure Description:** LED_PWM architecture diagram showing connections between High_Speed_Channel and Low_Speed_Channel components, including h_timer0 to h_ch7 for the HS channels (hschn) and l_timer0 to l_ch0 for the LS channels (lscrn).

**Footer:**
Espressif Systems
629 ESP32 TRM (Version 5.6)
Submit Documentation Feedback