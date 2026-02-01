**Title:**
1. Schematic Design

**Figure Caption (Top):**
Figure 1-3. Circuit for Splitting Ground Planes

**Subtitle and Body Text:**
1.2. Design Rules for Audio Chip

Each chip has its own design rules. For example, a codec might require very strict rules for digital and analog signals, otherwise unwanted noise might occur. Digital signal processors (DSP) might require different reference ground planes. Some PA power amplifiers can support different inputs, while others only single-ended input, etc.

**Note:**
In your design, you need to refer to the datasheet or reference design of the chips provided by the original manufacturer.
For example:
The specific design rules for a DSP:

**Subheading and Body Text (Highlighted in Red):**
DCDC/DIGITAL/MIC GROUNDS

Short PGND to DGND directly with a trace.

Short MGND to DGND directly with a trace
Do not use a resistor or ferrite between the grounds.
CX_PGND, CX_GND, CX_MGND: Create PGND plane, separate from normal (Digital Ground) planes for MGND. Tie the PGND to Digital ground planes together at C146/C150/Pin_6 junction using 30-mil trace.

**Figure Caption (Bottom):**
Figure 1-4. Reference Circuit Design for a DSP Ground Plane

The separation of AGND and DGND for a Codec:

**Footer:**
Espressif
3/19
2019.01