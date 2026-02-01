**Title: Functional Description**

---

### Section Title:
4.2.2.14 SD/MMC Host Controller (SDHOST)

#### Body Text:

ESP32-P4 has an SD/MMC Host Controller.

#### Feature List

- Two external cards
- SD memory Card specification v3.0 and v3.01
- Secure Digital I/O (SDIO 3.0)
- MMC: v4.41, v4.5, and v4.51
- CE-ATA: v1.1
- 1-bit, 4-bit, and 8-bit modes

#### Subtitle:
Pin Assignment

#### Body Text:

For the SD/MMC host controller, card one (SDMMC_HOST_SLOT_0) signals are multiplexed with GPIO39–GPIO48, the second RMII interface of EMAC, and the output signal of 50 MHz clock via IO MUX. Card two (SDMMC_HOST SLOT_1) signals can be routed to any GPIOs via the GPIO matrix.

For the SDIO2.0 interface, the pins can be chosen from any GPIOs via the GPIO Matrix.

---

### Section Title:
4.2.2.15 LED PWM Controller (LEDC)

#### Body Text:

The LED PWM Controller is a peripheral designed to generate PWM signals for LED control. It has specialized features such as automatic duty cycle fading. However, the LED PWM Controller can also be used to generate PWM signals for other purposes.

#### Feature List

- Eight independent PWM generators (i.e., eight channels)
- Maximum PWM duty cycle resolution: 20 bits
- Four independent timers that support fractional division
- Adjustable phase of PWM signal output
- PWM duty cycle dithering
- Automatic duty cycle fading — gradual increase/decrease of a PWM’s duty cycle without interference from the processor. An interrupt will be generated upon fade completion.
- Up to 16 duty cycle ranges for each PWM generator to generate gamma curve signals - each range can be independently configured in terms of fading direction (increase or decrease), fading amount (the amount by which the duty cycle increases or decreases each time), the number of fades (how many times the duty cycle fades in one range), and fading frequency
- PWM signal output in low-power mode (Light-sleep mode)
- Event generation and task response related to the Event Task Matrix (ETM) peripheral

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6