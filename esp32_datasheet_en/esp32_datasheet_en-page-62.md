**Title: Appendix A – ESP32 Pin Lists**

**Subtitle: Notes on ESP32 Pin Lists (A.1)**

---

**Table Title:** Table 6-1. Notes on ESP32 Pin Lists

| No. | Description |
|-----|-------------|
| **1** | In Table IO_MUX, the boxes highlighted in yellow indicate the GPIO pins that are input-only. Please see the following note for further details. <br> GPIO pins 34-39 are input-only. These pins do not feature an output driver or internal pull-up/pull-down circuitry. The pin names are: SENSOR_VP (GPIO36), SENSOR_CAPP (GPIO37), SENSOR_CAPN (GPIO38), SENSOR_VN (GPIO39), VDET_1 (GPIO34), VDET_2 (GPIO35). <br> The pins are grouped into four power domains: VDDA (analog power supply), VDD3P3_RTC (RTC power supply), VDD3P3_CPU (power supply of digital IOs and CPU cores), VDD_SDIO (power supply of SDIO IOs). VDD_SDIO is the output of the internal SDIO-LDO. The voltage of SDIO-LDO can be configured at 1.8V or be the same as that of VDD3P3_RTC. The strapping pin and eFuse bits determine the default voltage of the SDIO-LDO. Software can change the voltage of the SDIO-LDO by configuring register bits. For details, please see the column “Power Domain” in Table IO_MUX. |
| **4** | The functional pins in the VDD3P3_RTC domain are those with analog functions, including the 32 kHz crystal oscillator, ADC, DAC, and the capacitive touch sensor. Please see columns “Analog Function 0 ~ 2” in Table IO_MUX. |
| **5** | These VDD3P3_RTC pins support the RTC function, and can work during Deep-sleep. For example, an RTC-GPIO can be used for waking up the chip from Deep-sleep. <br> The GPIO pins support up to six digital functions, as shown in columns “Function 0 ~ 5” in Table IO_MUX. The function selection registers will set as “N”, where N is the function number. Below are some definitions: |
| **6** | SD_* is for signals of the SDIO slave. <br> HS1_* is for Port I signals of the SDIO host. <br> HS2_* is for Port 2 signals of the SDIO host. <br> MT* is for signals of the JTAG. <br> U0* is for signals of the UART0 module. <br> U1* is for signals of the UART1 module. <br> U2* is for signals of the UART2 module. <br> SPI* is for signals of the SPI01 module. <br> HSPI* is for signals of the SPI2 module. <br> VSPI* is for signals of the SPI3 module. |

---

**Footer:** Espressif Systems, ESP32 Series Datasheet v5.2

**Link:** Submit Documentation Feedback