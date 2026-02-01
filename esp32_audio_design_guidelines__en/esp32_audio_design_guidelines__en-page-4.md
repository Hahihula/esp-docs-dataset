Title: Schematic Design

Subtitle:
1.

Body Text:

The circuit design of an audio product, based on the ESP module provided by Espressif, can be broken down into three major sections:

- Power supply and GND plane.
- Design rules of audio chips.
- Pin configuration of the ESP32 module.

Subheading: 1.1. Power Supply and GND Plane

Sub-subheading:
1.1.1 USB/Battery Power Scheme

Body Text:

When the module works in Wi-Fi mode, peak current in the circuit is very high. The suggested output current for the module's power supply is no less than 500 mA. As audio boards generally require an external battery, your design may need a charging management chip, for example AP5056, to charge the battery. You can choose a chip according to your actual needs.

If the battery is used to power the whole system, please make sure that it is connected to the circuit and that the VBAT pin of the charging management chip, serving as the input of the system power supply, is connected to the positive terminal of the battery. As soon as the charging management chip detects the battery, it starts supplying current of the nominal value identified in its specification, but if the battery is not detected, the output current is very small, and power supply for the circuit may be insufficient.

You can avoid this problem by adding a USB/Battery power supply switch circuit into the design (as shown in Figure 1-1). For example, if a USB cable is plugged in, VBAT pin is cut off from the system and the power is supplied over USB; otherwise, the power will be supplied over VBAT.

Image Caption:
Figure 1-1. USB/Battery Power Supply Circuit

Footer: Espressif
Page Number: 1/19
Date: January 2019 (2019.01)