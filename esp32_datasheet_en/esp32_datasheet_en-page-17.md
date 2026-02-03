**Title: Pins**

---

### **2.3 IO Pins**

#### **2.3.1 Restrictions for GPIOs and RTC_GPIOs**

All IO pins of the ESP32 have GPIO and some have RTC_GPIO pin functions. However, these IO pins are multifunctional and can be configured for different purposes based on the requirements. Some IOs have restrictions for usage. It is essential to consider their multiplexed nature and the limitations when using these IO pins.

In Table 2-1 Pin Overview some pin functions are highlighted, specically:

- **GPIO** - Input only pins; output is not supported due to lack of pull-up/pull-down resistors.
- **GPIO** - allocated for communication with in-package flash/PSRAM and NOT recommended for other uses. For details, see Section 2.6 Pin Mapping Between Chip and Flash/PSRAM.

- **GPIO** - have one of the following important functions:
  - Strapping pins – need to be at certain logic levels at startup. See Section 3 Boot Configurations.
  - JTAG interface – often used for debugging.
  - UART interface – often used for debugging.

See also Appendix A.1 – Notes on ESP32 Pin Lists.

---

### **2.4 Analog Pins**

| Pin No. | Pin Name       | Pin Type   | Pin Function                                                                                   |
|---------|---------------|------------|------------------------------------------------------------------------------------------------|
| 2       | LNA_IN        | I/O        | Low Noise Amplifier (LNA) input signal, Power Amplifier (PA) output signal                       |
| 9       | CHIP_PU       | I          | High: on, enables the chip (Powered up).<br>Low: off, the chip powers off (powered down).    |
| 44      | XTAL_N        | —          | External clock input/output connected to chip’s crystal or oscillator.                         |
| 45      | XTAL_P        | —          | P/N means differential clock positive/negative.                                                |

---

### **2.5 Power Supply**

#### **2.5.1 Power Pins**

ESP32's digital pins are divided into three different power domains:

- VDD3P3_RTC
- VDD3P3_CPU
- VDD_SDIO

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32 Series Datasheet v5.2