

```markdown
Chapter 11 Low-Power Management

GoBack

Figure 11.4-1. ESP32-H2 Power Scheme

→: Control signals ——: Power lines


11.4.1.1 Regulators

As shown in Figure 11.4-1, the analog part of ESP32-H2 contains two regulators that regulate the power supply to different power domains. The two regulators are:

• One HP sys regulator, used for regulating the power supply to high-performance modules. It features strong drive capabilities, high power consumption, and regulated output power.
• One LP sys regulator, used for regulating the power supply to low-power modules. It also features regulated output power.

11.4.1.2 Digital Power Domains

ESP32-H2 has digital power domains as listed below. The HP system regulator powers the HP system, with a dedicated power switch located between the regulator and each individual power domain. This setup allows for independent control of the digital power domains. The LP sys regulator powers the LP system.

• The HP system contains the following digital power domains:

  – CPU: It mainly includes the CPU and its supporting peripherals (such as TRACE).
  – Modem: It consists of wireless MAC and baseband.
  – Peripherals + ROM: It mainly includes bus and HP peripherals.

Espressif Systems
389
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```