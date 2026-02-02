**Title:**
Chapter 8 Interrupt Matrix (INTERRUPT)

**Link:**
GoBack

**Subtitle:**
8.3.1 Peripheral Interrupt Source

**Body Text:**
ESP32 has 71 peripheral interrupt sources in total. All peripheral interrupt sources are listed in table **8.3-1**. Of these, ESP32 peripheral interrupt sources can be allocated to either CPU.

The four remaining peripheral interrupt sources are CPU-specific, two per CPU. GPIO INTERRUPT_PRO and GPIO_INTERRUPT_PRO_NMI can only be allocated to PRO_CPU. GPIO_INTERRUPT_APP and GPIO_INTERRUPT_APP_NMI can only be allocated to APP_CPU. As a result, PRO_CPU and APP_CPU each have 69 peripheral interrupt sources.

**Link:**
PeripheralInterruptConfigStatusSource.tex

**Footer Information:**
Espressif Systems
175 ESP32 TRM (Version 5.6)
Submit Documentation Feedback