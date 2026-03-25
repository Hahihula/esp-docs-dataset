

```markdown
Chapter 11 Low-Power Management

GoBack

• Analog power domains
• Digital power domains

Figure 11.4-1 ESP32-C61 Power Scheme

11.4.1.1 Regulators

As shown in Figure 11.4-1, the analog part of ESP32-C61 contains two sets of regulators that regulate the power supply to different power domains. The two regulators are:

• One set of HP system regulators:
    – one main HP regulator
    – two secondary HP regulators powering the HP memory and HP logic circuits respectively.

They are used for regulating the power supply to high-performance modules and feature high drive strength, high power consumption, and regulated output power.

• One set of LP system regulators:
    – one main LP regulator
    – one secondary LP regulator

Espressif Systems                           496                          ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback               PRELIMINARY
```