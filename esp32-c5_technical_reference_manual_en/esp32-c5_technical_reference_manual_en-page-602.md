

```markdown
Chapter 13 Low-Power Management

• Analog power domains
• Digital power domains

Figure 13.4-1. ESP32-C5 Power Scheme

13.4.1.1 Regulators

As shown in Figure 13.4-1, the analog part of ESP32-C5 contains two regulators that regulate the power supply to different power domains. The two regulators are:

• HP sys regulator, used for regulating the power supply to the HP system. It features strong drive capability, higher power consumption, and adjustable output voltage.
• LP sys regulator, used for regulating the power supply to the LP system. Its output voltage is also adjustable.

13.4.1.2 Digital Power Domains

• The HP system contains the following digital power domains:

  – CPU: It mainly includes the CPU and its supporting peripherals (such as TRACE).
  – Modem: It consists of wireless MAC and baseband.
```