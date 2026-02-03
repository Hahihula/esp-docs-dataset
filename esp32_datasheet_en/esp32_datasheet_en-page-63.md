**Appendix A**

---

### No. Description

Each column about digital “Function” is accompanied by a column about “Type”. Please see the following explanations for the meanings of “type” with respect to each “function” they are associated with.

For each "Function-N", "type" signifies:
- **I:** input only.
  - If a function other than “Function-N” is assigned, the input signal of “Function-N” is still from this pin.
- **II:** input only. 
  - If a function other than “Function-N” is assigned, the input signal of “Function-N” is always “1”.
- **IO:** input only.
  - If a function other than “Function-N” is assigned, the input signal of “Function-N” is always “0”.

**O:** output only.

**T:** high-impedance

**I/O/T:** combinations of input, output, and high-impedance according to the function signal.
- **II/O/T:** combinations of input, output, and high-impedance, according to the function signal. If a function is not selected, the input signal of the function is “1”.

For example, pin 30 can function as HS1_CMD or SD_CMD, where HS1_CMD is of an “I/O/T” type.
If pin 30 is selected as HS1_CMD, this pin’s input and output are controlled by the SDIO host. If pin 30 is not selected as HS1_CMD, the input signal of the SDIO host is always “1”.

Each digital output pin is associated with its configurable drive strength. Column "Drive Strength" in Table IO_MUX lists the default values.
The drive strength of the digital output pins can be configured into one of the following four options:
- **0:** ~5 mA
- **1:** ~10 mA
- **2:** ~20 mA
- **3:** ~40 mA

The default value is 2.

The internal pull-up (wpu) and pull-down (wpd) are ~75 μA.
During reset, all pins are output-disabled. 

### Column “At Reset” in Table IO_MUX lists the status of each pin during reset
- **Column "After Reset"** in Table IO_MUX lists the statuses immediately after reset:
  - Including input-enabled (ie=1), internal pull-up (wpu) and internal pull-down (wpd). After reset, each pin is set to “Function O”. The output-enable is controlled by digital Function.

### Column Ethernet_MAC
- **Table Ethernet_MAC** about signal mapping inside Ethernet MAC.
  - Supports MI2 and RMII interfaces,
  - Supports both the internal PLL clock and external clock source. For MII interface:
    - Ethernet MAC with/TX_ERR signal, MDIO, CRS, and COL are slow signals.

### Column GPIO Matrix
- **Table GPIO Matrix** is for the GPIO-Matrix.
  - The on-chip functional modules can be mapped onto any GPIO pin,
  - Some signals may map to a pin by both IO-MUX and GPIO-Matrix as shown in column tagged “Same input signal from IO_MUX core”:
    - In Table GPIO Matrix.

---

Espressif Systems  
63  
ESP32 Series Datasheet v5.2

Submit Documentation Feedback