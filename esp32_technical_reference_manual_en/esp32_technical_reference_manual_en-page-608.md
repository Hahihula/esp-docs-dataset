**Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Menu/Navigation Link:**
GoBack

**Table with Legend and Parameters:**

| Parameter | Description |
|-----------|-------------|
| t<sub>OH</sub> | Output Hold Time in HS Mode |
| f<sub>PP</sub> = 80 MHz | Clock frequency in data transfer mode. |
| 0.5 ns | - |

**Legend (continued):**
- f<sub>PP</sub> - Clock frequency in data transfer mode.
- t<sub>W(CKL)/t<sub>W(CKH)</sub> - Clock Low/High Time: t<sub>W(CKL)/t<sub>W(CKH)</sub> represents the time that the clock signal (CK) should remain in the low or high state.
- t<sub>ISU</sub> - Input Setup Time in HS Mode; t<sub>ISU</sub> represents the setup time required for CMD and D (data lines) inputs.
- t<sub>IH</sub> - Input Hold Time in HS Mode: t<sub>IH</sub> specifies the hold time required for CMD and D inputs.
- t<sub>OV</sub> - Output Valid Time in HS Mode; defines the time it takes for the CMD and D outputs to be ready.
- t<sub>OH</sub> - Output Hold Time in HS Mode: t<sub>OH</sub> specifies the hold time required for the CMD and D outputs to be valid.

**Bullet Point Note:**
The timing of the CMD and D inputs and outputs are measured in relation to the clock signal CK.

**Subheading:**

27.11 Clock Phase Selection

**Body Text:**
If the setup time requirements for the input or output data signal are not met, users can specify the clock phase, as shown in the figure below:

**Image Description (Figure 27.11-1):**
Clock Phase Selection diagram showing different phases and their corresponding bits.

**Footer Note:**
Please find detailed information on the clock phase selection register CLK_EDGE_SEL in Section Registers.

**Company Information at Bottom of Page:**
Espressif Systems

**Document Version Info:**
ESP32 TRM (Version 5.6)

**Feedback Link:**
Submit Documentation Feedback