Title: Power Scheme for Peripherals

Subtitle: Schematic Design (1)

Body Text:
Peripherals that require power supply on an audio board include Wi-Fi module, Codec module, DSP module, PA power amplifier module, Micro SD card module, LED module, etc. While PA power amplifier is directly powered by USB/Battery, the other modules are powered through the power management chip, which converts the USB/Battery voltage to the voltage they require.

For increased reliability, you can reserve a separate power management chip and optional resistors for each module in case an independent (backup) power supply is needed. During debugging, you can determine whether some chips can be removed, based on the actual test results. The power management chip of your choice should meet the circuit requirements for input and output of current and voltage, low noise, efficiency and other aspects of the circuit.

For example:

Image Description:
- Figure 1-2: Power Supply Management Circuit for Peripherals

Subtitle: Ground Plane Splitting Scheme (1)

Body Text:
For the above-listed modules (Wi-Fi module, Codec module, DSP module, PA power amplifier module, Micro SD card module, LED module, etc.), their reference ground planes should be separated according to the actual situation. For example, the reference ground plane of Wi-Fi module and Micro SD card is DGND; the reference ground plane for PA power amplifier and external loudspeaker is AGND; Codec module, DSP module, LED light and other chips also have their own reference ground planes. It is also recommended to provide a separate ground plane for the input power module. These planes should be connected by a short circuit with a 0R resistor (Packaging should be above 0603), such as at the following figure:

Footer:
- Page number: Espressif
- Document page count and date reference: 2/19, January 2019

(Note: The image of Figure 1-2 is described but not transcribed due to its graphical nature.)