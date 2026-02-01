**Title: Advanced Peripheral Interfaces**

- **19 programmable GPIOs**
  - Three strapping pins: GPIO8, GPIO9, and GPIO25

- Digital interfaces:
  - Two SPI ports for communication with flash
  - General-purpose SPI port
  - Two UART
  - Two I2C
  - I2S
  - RMT, with up to 2 transmit channels and 2 receive channels
  - Pulse count controller
  - LED PWM controller, up to 6 channels
  - USB Serial/JTAG controller
  - Motor Control PWM (MCPWM)
  - General DMA controller, with 3 transmit channels and 3 receive channels
  - TWAI® controller, compatible with ISO 11898-1 (CAN Specification 2.0)
  - SoC event task matrix (ETM)
  - Parallel IO (PARLIO) controller

- Analog interfaces:
  - 12-bit SAR ADC, up to 5 channels
  - Temperature sensor

- Timers:
  - Two 54-bit general-purpose timers
  - 52-bit system timer
  - Three watchdog timers

**Title: Power Management**

Fine-resolution power control through a selection of clock frequency, duty cycle, RF operating modes, and individual power control of internal components.

Four power modes designed for typical scenarios: Active, Modem-sleep, Light-sleep, Deep-sleep

Power consumption in Deep-sleep mode is 7 μA

LP memory remains powered on in Deep-sleep mode

**Footer:**  
Espressif Systems  
4  
Submit Documentation Feedback  
ESP32-H2 Series Datasheet v1.2