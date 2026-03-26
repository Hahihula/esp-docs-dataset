

```markdown
Chapter 14 Low-Power Management

GoBack

• Two internal regulators
• Four output regulators (EXT_LDO)
• Analog power domains
• Digital power domains
• Battery power domain


Figure 14.4-1. ESP32-P4 Power Scheme

--->: Control signals ----: Power lines

14.4.1.1 Regulators

As shown in Figure 14.4-1, the analog section of ESP32-P4 includes one external DCDC with feedback regulation and two internal HP/LP system regulators, responsible for regulating the power supply for different power domains.

• The DCDC voltage regulation feedback system adjusts the voltage of the external DCDC.
```