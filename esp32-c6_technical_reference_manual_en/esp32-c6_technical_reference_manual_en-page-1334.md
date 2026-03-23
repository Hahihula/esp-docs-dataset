

```markdown
Chapter 38 Parallel IO Controller (PARL_IO) GoBack


Figure 38.5-2. Master Clock Positive Waveform



• Scenario 3: The clock sent by the master device is not a free-running clock, and the clock waveform is as shown in Figure 38.5-3.
Requirement: The master device should invert the original clock and convert it to the waveform as Figure 38.5-2 shows before output.



Figure 38.5-3. Master Clock Negative Waveform



For the RX unit which can only function as slave, the following three scenarios can occur:

• Scenario 1: The clock sent by the master device is a free-running clock.
Requirement: There is no requirement for the acquisition edge of the master clock, and the valid data is subject to the external enable signal.

• Scenario 2: The clock sent by the master device is not a free-running clock, and the clock waveform is as shown in Figure 38.5-2.
Requirement: It is required for the master device to drive the data at the rising edge and the RX unit to capture the data at the falling edge (i.e., to inverse the master clock).

• Scenario 3: The clock sent by the master device is not a free-running clock, and the clock waveform is as shown in Figure 38.5-3.
Requirement: It is required for the master device to drive the data at the falling edge and the RX unit to capture the data at the rising edge (i.e., to use the original master clock).



38.5.4 Receive Modes of the RX Unit

PARLIO supports 15 receive modes, which can be divided into three major categories according to the enable signal:

• Level Enable mode: data received is enabled by the external signal level;
• Pulse Enable mode: data received is enabled by the external signal pulse;
• Software Enable mode: the enable signal of data received can be configured by users directly.



38.5.4.1 Level Enable Mode

Level Enable mode can be divided into two sub-modes depending on the active level of the external enable signal, as shown in Figure 38.5-4.

In both cases, an active level on the external enable signal must be aligned with valid data. Since the external level enable signal occupies one IO pin, there are at most 15 IO pins left usable for RXD.
```